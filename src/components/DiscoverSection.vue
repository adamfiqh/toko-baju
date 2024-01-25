<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="discover-section">
    <img
      :src="discoverImageUrl"
      :alt="discoverImageAlt"
      class="discover-image"
    />
    <div class="discover-text">{{ discoverText }}</div>
    <div class="discover-subtext">Casual & Minimalist</div>
    <div class="gradient-overlay"></div>
  </div>
</template>

<script>
export default {
  props: {
    discoverImageUrl: String,
    discoverImageAlt: String,
    discoverText: String,
    gradientImageUrl: String,
  },
};
</script>

<style scoped>
/* styles here */
</style>

<style scoped>
.discover-section {
  position: relative;
  margin-bottom: 20px;
}

.discover-image {
  width: 100%;
  border-radius: 30px;
}

.discover-text {
  position: absolute;
  top: 20px;
  left: 20px;
  color: #fff;
  font-size: 36px;
  font-family: "Clash Display", sans-serif;
  font-weight: 500;
  word-wrap: break-word;
}

.discover-subtext {
  position: absolute;
  top: 70px;
  left: 20px;
  color: #fff;
  font-size: 24px;
  font-family: "Clash Display", sans-serif;
  font-weight: 500;
  letter-spacing: 1.25px;
  word-wrap: break-word;
}

.gradient-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(180deg, rgba(35, 70, 136, 0) 0%, #214195 100%);
  border-radius: 30px;
}
</style>
