<script setup lang="ts">
  const data = [
    {
      id: 1,
      image: 'https://i.ebayimg.com/images/g/yawAAOSwpqdc~dft/s-l1600.jpg'
    },
    {
      id: 2,
      image: 'https://i.ebayimg.com/images/g/yawAAOSwpqdc~dft/s-l1600.jpg'
    },
    {
      id: 3,
      image: 'https://i.ebayimg.com/images/g/yawAAOSwpqdc~dft/s-l1600.jpg'
    },
    {
      id: 4,
      image: 'https://i.ebayimg.com/images/g/yawAAOSwpqdc~dft/s-l1600.jpg'
    },
  ]
</script>

<template>
  <div :class="$style.promo">
    <div  v-for="(item, index) in data" :key="item.id">
      <img :src="item.image" alt="promo">
    </div>
  </div>
</template>

<style module lang="scss">
  .promo {
    width: 300px;
    display: flex;
    flex-direction: column;
    gap: 20px;

    img {
      width: 100%;
    }
  }
</style>