<script setup lang="ts">
  interface IProps {
    title: string;
    time: string;
    image: string;
  };

  const props = defineProps<{ data: IProps }>();

  const { data } = props;

</script>

<template>
  <div :class="$style.otherNews">
    <div :class="imageContainer">
      <img :class="$style.img" :src="data.image" :alt="data.title">
    </div>
    <div :class="$style.info">
      <p :class="$style.title">
        {{ data.title }}
      </p>
      <span :class="$style.time">
        {{ data.time }}
      </span>
    </div>
  </div>
</template>

<style module lang="scss">
  .otherNews {
    display: flex;
    justify-content: space-between;
    background: rgb(219, 220, 221) 86% 13%;
    padding: 16px;
    border-radius: 20px;
    gap: 10px;

    .imageContainer {

    }

    .img {
      width: 87px;
      height: 58px;
    }

    .info {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      .title {
        font-family: 'Manrope';
        font-size: 14px;
        font-weight: 700;
        line-height: 16.24px;
        text-align: left;
        color: rgba(0, 0, 0, 1);
      }

      .time {
        display: flex;

        font-family: 'Cousine';
        font-size: 10px;
        font-weight: 400;
        line-height: 12px;
        letter-spacing: 0.06em;
        text-align: left;
        opacity: 0.5;
        text-transform: uppercase;
      }
    }
  }
</style>