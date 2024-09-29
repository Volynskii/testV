<script setup lang="ts">
  defineProps({
    text: {
      type: String,
      default: '',
      required: true
    }
  })
</script>

<template>
  <div :class="$style.paragraph">
    <p>
      {{ text }}
    </p>
  </div>
</template>

<style module lang="scss">
  .paragraph {
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 22px;
    color: #000000;
  }
</style>