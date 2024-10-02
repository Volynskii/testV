<script setup lang="ts">

import logo from '@/assets/images/logo.svg';

const props = defineProps({
  image: {
    type: String,
    default: '',
    required: false
  },
  title: {
    type: String,
    default: '',
    required: false
  },
  description: {
    type: String,
    default: '',
    required: false
  },
  time: {
    type: String,
    default: '',
    required: false
  }
});

const stylesBg = props.image && {marginRight: '170px', marginBottom: '20px'};

</script>

<template>
  <div :class="$style.newFeedHead">
    <div :class="$style.bg" :style="{...stylesBg}">
      <div :class="$style.container">
        <div :class="$style.logo">
          <img :src="logo" alt="logo">
        </div>
        <div :class="$style.header">
          <span>{{ time }}</span>
        </div>
        <div :class="$style.content">
          <div :class="$style.top">
            {{ title }}
          </div>
          <div :class="$style.bottom">
            {{ description }}
          </div>
        </div>
      </div>
    </div>
    <div v-if="image" :class="$style.image">
      <img :src="image" :alt="title">
    </div>
  </div>
</template>

<style module lang="scss">
  .newFeedHead {
    position: relative;
    display: inline-block;
    min-width: 295px;

    .image {
      width: 262px;
      height: 100%;
      position: absolute;
      right: 0px;
      top: 0px;
      z-index: 0;

      img {
        width: 100%;
        height: 100%;
      }
    }


    .bg {
      background-image: url('https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/6.jpg');
      background-size: cover;
      margin: 20px 0 0 0px;
      max-width: 295px;
      position: relative;
      z-index: 1;

      .container {
        backdrop-filter: blur(40px);
        padding: 16px 16px 24px 16px;
        margin-top: 20px;

        .logo {
          position: absolute;
          width: 60px;
          height: 60px;
          top: -20px;
          right: 32px;
        }

        .header {
          margin-bottom: 32px;
          color: rgba(255, 255, 255, 1);
          font-size: 12px;
          font-family: 'Cousine';
          font-weight: 400;
          line-height: 15px;
          opacity: 0.8;
        }

        .content {

          .top {
            color: rgba(255, 255, 255, 1);
            font-size: 21px;
            font-weight: 700;
            line-height: 23px;
            letter-spacing: -0.5px;
            margin-bottom: 56px;
          }

          .bottom {
            color: rgba(255, 255, 255, 1);
            font-size: 14px;
            font-weight: 400;
            line-height: 19px;
            opacity: 0.75;
          }
        }
      }
    }
  }
</style>