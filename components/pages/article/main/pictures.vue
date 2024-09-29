<script setup lang="ts">

defineProps({
  description: {
    type: String,
    default: '',
    required: true
  },
  name: {
    type: String,
    default: '',
    required: true
  },
  position: {
    type: String,
    default: '',
    required: true
  },
})

</script>

<template>
  <div :class="$style.pictures">
    <div :class="$style.picture">
      <PagesArticleMainSliders/>
    </div>
    <div :class="$style.info">
      <span>
        {{ description }}
      </span>

      <div>
          <span>
            {{ name }}
          </span>
          /
          <span>
            {{ position }}
          </span>
      </div>
    </div>
  </div>
</template>

<style module lang="scss">
  .pictures {
    .picture {

    }

    .info {
    }


  }
</style>