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
      <span :class="$style.slash">/</span>
      <span :class="$style.person"> {{ person }}</span>
    </div>
    <div :class="$style.right">
      <span>{{ topic }}</span>
    </div>
  </div>
</template>

<style module lang="scss">
  .info {
    display: flex;
    justify-content: space-between;
    margin: 0 52px 0 52px;
    text-transform: uppercase;

    .left {
      font-family: 'Cousine';
      text-align: left;
      color: rgba(0, 0, 0, 1);
      display: flex;
      gap: 8px;

      .created {
        font-size: 10px;
        font-weight: 400;
        line-height: 12px;
        letter-spacing: 0.06em;
      }
      .updated {
        font-size: 10px;
        font-weight: 400;
        line-height: 12px;
        letter-spacing: 0.06em;
        opacity: 0.4;
      }
      .person, .slash {
        font-size: 10px;
        font-weight: 400;
        line-height: 12px;
        letter-spacing: 0.06em;
        text-align: center;
      }
    }
    .right {
      font-size: 10px;
      font-weight: 400;
      line-height: 12px;
      letter-spacing: 0.06em;
      text-align: right;
    }
  }
</style>