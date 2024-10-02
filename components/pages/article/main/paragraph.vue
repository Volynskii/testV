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
  <p :class="$style.paragraph">
    {{ text }}
  </p>
</template>

<style module lang="scss">
  .paragraph {
    display: inline;
    font-size: 17px;
    font-weight: 400;
    line-height: 22.1px;
    text-align: left;
  }
</style>