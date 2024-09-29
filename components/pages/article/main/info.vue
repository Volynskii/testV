<script setup lang="ts">

defineProps({
  created: {
    type: String,
    default: '',
    required: true
  },
  updated: {
    type: String,
    default: '',
    required: true
  },
  person: {
    type: String,
    default: '',
    required: true
  },
  topic: {
    type: String,
    default: '',
    required: true
  }
})

</script>

<template>
  <div :class="$style.info">
    <div :class="$style.left">
      <span :class="$style.created">{{ created }}</span>
      <span :class="$style.updated">{{ updated }}</span>
      <span :class="$style.person">/ {{ person }}</span>
    </div>
    <div :class="$style.right">
      <span>{{ topic }}</span>
    </div>
  </div>
</template>

<style module lang="scss">
  .info {
    .left {
      .created {
        // font-style: normal;
        // font-weight: 400;
        // font-size: 12px;
        // line-height: 16px;
        // color: #A0A0A0;
      }
      .updated {
      }
      .person {
      }
    }
    .right {

    }
  }
</style>