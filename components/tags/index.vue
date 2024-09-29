<script setup lang="ts">
  import arrow from '@/assets/images/tag-next_arrow.svg';
  
  interface IData {
    id: number;
    name: string;
  };

  defineProps({
    data: {
      type: Array as () => IData[],
      default: () => [],
      required: true
    }
  });

</script>

<template>
  <div :class="$style.tags">
    <template v-for="(item, index) in data" :key="item.id">
      <TagsItem :topic="item.name" :now-topic="data[0].name"/>
    </template>

    <div :class="$style.next">
      <img :src="arrow" alt="next">
    </div>
  </div>
</template>

<style module lang="scss">
  .tags {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 4px;

    font-family: Cousine;
    font-size: 12px;
    font-weight: 400;
    line-height: 16.8px;
    text-transform: uppercase;

    .next {
      border-radius: 50%;
      background: rgba(245, 245, 245, 1);
      width: 40px;
      height: 40px;
      display: flex;
      justify-content: center;
      align-items: center;
    }
  }
</style>