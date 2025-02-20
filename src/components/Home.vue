<script setup>
import MyImage from '../assets/MyImage.webp'
</script>
<template>
  <div class="hero" id="home">
    <img :src="MyImage" alt="img" />
    <h1> Alan Walker</h1>
    <p>Web and Mobile App Developer </p>
  </div>
</template>
<style scoped>
.hero img {
  object-fit: cover;
  width: 100%;
  height: 640px;
  position: relative
}

.hero h1 {
  color: white;
  position: absolute;
  top: 250px;
  left: 120px;
  font-size: 80px;
  font-weight: bolder;
}

.hero p {
  color: white;
  position: absolute;
  top: 360px;
  left: 120px;
  font-size: 22px;

}

@media (max-width:557px) {
  .hero h1 {
    color: white;
    position: absolute;
    top: 250px;
    left: 40px;
    font-size: 80px;
    font-weight: bolder;
  }

  .hero p {
    color: white;
    position: absolute;
    top: 425px;
    left: 40px;
    font-size: 22px;

  }
}
</style>
