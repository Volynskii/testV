
<script setup lang="ts">
  const dataNewsFeed = [
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
  ];
</script>

<template>
  <div :class="$style.article">
    <div :class="$style.articleWrapper">
      <NewsFeed :data="dataNewsFeed" />
      <PagesArticleMain />
      <PagesArticlePromo />
    </div>
  </div>
</template>

<style module lang="scss">
  .article {

    &Wrapper {
      display: flex;
      flex-wrap: nowrap;
      gap: 20px;
      margin-left: 20px;
    }
  }
</style>
