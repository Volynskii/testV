
<script setup lang="ts">

const data = [
  {
    id: 1,
    title: 'Кнайсль: ФРГ не осознает, что для россиян значат немецкие машины ВСУ под Курском',
    image: 'https://cdn-st1.smotrim.ru/vh/pictures/lw/407/643/9.jpg',
    description: 'Росгвардейцы с помощью беспилотника обнаружили стартовые позиции ударных БПЛА ВСУ',
    topic: 'политика',
    time: '2022-07-25T14:30:00.000Z',
  },
  {
    id: 2,
    title: 'Кнайсль: ФРГ не осознает, что для россиян значат немецкие машины ВСУ под Курском',
    image: 'https://cdn-st1.smotrim.ru/vh/pictures/lw/407/643/9.jpg',
    description: 'Росгвардейцы с помощью беспилотника обнаружили стартовые позиции ударных БПЛА ВСУ',
    topic: 'политика',
    time: '2022-07-25T14:30:00.000Z',
    urgently: true
  },
  {
    id: 3,
    title: 'Самолет из Хабаровска с задымлением готовится к аварийной посадке',
    image: 'https://cdn-st1.smotrim.ru/vh/pictures/lw/407/643/9.jpg',
    description: 'Росгвардейцы с помощью беспилотника обнаружили стартовые позиции ударных БПЛА ВСУ',
    topic: 'политика',
    time: '2022-07-25T14:30:00.000Z',
    urgently: false
  }
]

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
    max-width: 465px;
    background: white;

    padding-top: 20px;
  }
</style>