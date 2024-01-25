<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <ProductItem
      v-for="(product, index) in products"
      :key="index"
      :image-url="product.image"
      :product-name="product.name"
      :product-price="`Rp. ${product.price}`"
      :is-on-sale="product.isOnSale"
    />
    <HomeView
      :discover-image-url="discoverImageUrl"
      :discover-image-alt="discoverImageAlt"
      :discover-text="discoverText"
      :gradient-image-url="gradientImageUrl"
    />
  </div>
</template>

<script>
import axios from "axios";
import ProductItem from "@/components/Product.vue";
import HomeView from "@/components/DiscoverSection.vue";

export default {
  components: {
    ProductItem,
    HomeView,
  },
  data() {
    return {
      products: [],
      discoverImageUrl: "https://via.placeholder.com/545x595",
      discoverImageAlt: "Discover Section",
      discoverText: "Discover The Latest Trend in Fashion",
      gradientImageUrl: "https://via.placeholder.com/488x252",
    };
  },
  mounted() {
    this.fetchProducts();
  },
  methods: {
    async fetchProducts() {
      try {
        const response = await axios.get(
          "https://sistemtoko.com/public/demo/product"
        );
        this.products = response.data;
      } catch (error) {
        console.error("Error fetching products:", error);
      }
    },
  },
};
</script>

<style scoped>
/* styles here */
</style>
