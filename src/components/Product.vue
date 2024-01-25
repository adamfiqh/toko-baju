<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="product-container">
    <div class="product-image">
      <img :src="imageUrl" :alt="productName" />
    </div>
    <div class="sale-tag" v-if="isOnSale">Sale</div>
    <div class="product-details">
      <div class="product-name">{{ productName }}</div>
      <div class="product-price">{{ productPrice }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    imageUrl: String,
    productName: String,
    productPrice: String,
    isOnSale: Boolean,
  },
};
</script>

<style scoped>
.product-container {
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

.product-image img {
  max-width: 100%;
  height: auto;
  border-bottom: 1px solid #ddd;
}

.sale-tag {
  position: absolute;
  top: 10px;
  left: 10px;
  padding: 8px;
  background: #e95144;
  color: #f0f4ff;
  font-size: 16px;
  font-weight: 400;
}

.product-details {
  text-align: center;
}

.product-name {
  color: #252525;
  font-size: 14px;
  font-family: "Poppins", sans-serif;
  font-weight: 400;
  letter-spacing: 0.15px;
  word-wrap: break-word;
}

.product-price {
  color: #214195;
  font-size: 18px;
  font-family: "Poppins", sans-serif;
  font-weight: 500;
  letter-spacing: 0.15px;
  word-wrap: break-word;
}
</style>
