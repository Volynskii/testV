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
      <span :class="$style.description">
        {{ description }}
      </span>

      <div :class="$style.person">
          <span>
            фото: {{ name }}
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

      .description {
        font-family: 'NunitoSans';
        font-size: 14px;
        font-weight: 400;
        line-height: 16.24px;
        display: block;
        margin: 12px 0;
      }

      .person {
        text-transform: uppercase;
        font-family: 'Cousine';
        font-size: 10px;
        font-weight: 400;
        line-height: 13px;
        letter-spacing: 0.06em;
        opacity: 0.5;
      }
    }


  }
</style>