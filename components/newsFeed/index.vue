
<script setup lang="ts">

interface IData {
  id: number;
  title: string;
  image: string;
  description: string;
  topic: string;
  time: string;
  urgently?: boolean;
}

defineProps({
  data: {
    type: Array as ()=> IData[],
    default: () => [],
    required: true
  }
});

function getTime(time: string): string {
  const date = new Date(time);
  return date.getHours() + ':' + date.getMinutes();
};
</script>

<template>
  <div :class="$style.newsFeed">

    <div>
      <NewsFeedHead :title="data[0].title" :description="data[0].description" :time="getTime(data[0].time)"/>
    </div>

    <div>
      <template v-for="(item, index) in data" :key="item.id">
        <NewsFeedItem :urgently="item.urgently" :title="item.title"  :topic="item.topic" :time="getTime(item.time)"/>
      </template>
    </div>
  </div>
</template>

<style module lang="scss">
  .newsFeed {
    // max-width: 465px;
    max-width: 295px;
    background: white;
    padding-top: 20px;
  }
</style>