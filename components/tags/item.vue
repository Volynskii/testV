<script setup lang="ts">
  defineProps({
    topic: {
      type: String,
      default: '',
      required: true
    },
    nowTopic: {
      type: String,
      default: '',
      required: true
    }
  })
</script>

<template>
  <div :class="[$style.tag, nowTopic === topic && $style.tagActive]">
    <span>{{ topic }}</span>
  </div>
</template>

<style module lang="scss">
  .tag {
    padding: 16px 14px;
    background: rgba(245, 245, 245, 1);
    border-radius: 50px;

    &Active {
      color: rgba(0, 0, 255, 1);
    }
  }
</style>