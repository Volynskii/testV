<script setup lang="ts">

  const props = defineProps({
    title: {
      type: String,
      default: '',
      required: true
    },
    image: {
      type: String,
      default: '',
      required: false
    },
    topic: {
      type: String,
      default: '',
      required: true
    },
    time: {
      type: String,
      default: '',
      required: true
    },
    urgently: {
      type: Boolean,
      default: false,
      required: false
    }
  });

</script>

<template>
  <div :class="[$style.newFeedItem, urgently && $style.urgently]">
    <div :class="$style.content">
      <div :class="$style.header">
        <span>{{ time }}</span>
        <span>{{ topic }}</span>
      </div>

      <div :class="$style.description">
        <p>{{ title }}</p>
      </div>
    </div>

    <template v-if="image">
      <div :class="$style.image">
        <img :src="image" :alt="topic">
      </div>
    </template>
  </div>
</template>

<style module lang="scss">
  .newFeedItem.urgently {
    color: rgba(204, 0, 0, 1);

    &::before {
      background: rgba(204, 0, 0, 1);
    }

    .description::before {
      content: url('@/assets/images/lightning.svg');
      margin-right: 8px;
    }
  }

  .newFeedItem {
    padding: 0px 0px 0 10px;
    display: flex;
    flex-wrap: nowrap;
    height: 105px;
    margin: 3px 0;
    color: rgba(0, 0, 0, 1);
    position: relative;

    &::before {
      content: '';
      position: absolute;
      left: 0;
      width: 2px;
      height: 100%;
      background: rgba(0, 0, 255, 1);
    }

    .content {
      min-width: 267px;
      padding-right: 12px;
      margin-top: 24px;
    }

    .header {
      display: flex;
      justify-content: space-between;
      margin-bottom: 12px;
      font-family: 'Cousine';
      font-size: 10px;
      line-height: 12px;
      font-weight: 400;
      opacity: 0.5;
    }

    .description {
      font-weight: 600;
      font-size: 16px;
      line-height: 18.56px;
      display: flex;
    }

    .image {
      height: 100%;
      min-width: 170px;

      img {
        width: 100%;
        height: 100%;
      }
    }
  }
</style>