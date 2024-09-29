<script setup lang="ts">
import type { PropType } from 'vue';

const props = defineProps({
  newsFeedData: {
    type: Array as PropType<Array<{
      id: number;
      title: string;
      image: string;
      description: string;
      topic: string;
      time: string;
      urgently?: boolean;
    }>>,
    required: true,
  }
});

function getTime(time: string): string {
  const date = new Date(time);
  return date.getHours() + ':' + date.getMinutes();
}
</script>

<template>
  <div :class="$style.newsFeed">

    <div v-if="newsFeedData.length">
      <NewsFeedHead :title="newsFeedData[0].title" :description="newsFeedData[0].description" :time="getTime(newsFeedData[0].time)"/>
    </div>

    <div>
      <template v-for="({urgently, title, topic, time, image}) in newsFeedData" :key="item.id">
        <NewsFeedItem :urgently="urgently" :title="title"  :topic="topic" :time="getTime(time)" :image="image"/>
      </template>
    </div>

    <!-- Слот для кнопки -->
    <slot name="newsFeedButton"></slot>

  </div>
</template>

<style module lang="scss">
.newsFeed {
  max-width: 465px;
  background: white;
  padding-top: 20px;
}
</style>
