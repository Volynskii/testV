<script setup lang="ts">
  import social_1 from '@/assets/images/sm/vk.svg';
  import social_2 from '@/assets/images/sm/ok.svg';
  import social_3 from '@/assets/images/sm/tg.svg';
  import social_4 from '@/assets/images/sm/yd.svg';
  import social_5 from '@/assets/images/sm/tt.svg';

  const sm = [
    {
      id: 1,
      src: social_1,
      name: 'vk',
      link: 'https://vk.com'
    },
    {
      id: 2,
      src: social_2,
      name: 'vk',
      link: 'https://vk.com'
    },
    {
      id: 3,
      src: social_3,
      name: 'vk',
      link: 'https://vk.com'
    },
    {
      id: 4,
      src: social_4,
      name: 'vk',
      link: 'https://vk.com'
    },
    {
      id: 5,
      src: social_5,
      name: 'vk',
      link: 'https://vk.com'
    },
  ]
</script>

<template>
  <div :class="$style.sm">
    <div :class="$style.text">
      <span>ИА Вести</span>
      <span>в соцсетях</span>
    </div>

    <div :class="$style.icons" >
      <div :class="$style.item" v-for="item in sm" :key="item.name">
        <img :src="item.src" :alt="item.name" :aria-label="item.name" />
      </div>
    </div>
  </div>
</template>

<style module lang="scss">
  .sm {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
  }

  .text {
    display: flex;
    flex-direction: column;

    font-family: 'Cousine';
    font-size: 12px;
    font-weight: 700;
    line-height: 13.2px;
    text-align: left;

    span {
      display: block;
    }

    span:first-child {
      color: rgba(0, 0, 255, 1);
    }
  }

  .icons {
    display: flex;
    flex-wrap: nowrap;

    .item {
      padding: 8px 12px;
      background: rgba(245, 245, 245, 1);
      border-radius: 50px;

      img {
        width: 24px;
        height: 24px;
      }
    }
  }
</style>