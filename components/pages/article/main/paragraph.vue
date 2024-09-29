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
    font-size: 17px;
    font-weight: 400;
    line-height: 22.1px;
    text-align: left;
  }
</style>