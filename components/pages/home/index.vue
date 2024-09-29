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
];
</script>

<template>
  <div :class="$style.article">
    <div :class="$style.newsFeed">
      <!-- Передаем data через пропс newsFeedData -->
      <PagesArticleNewsFeed :newsFeedData="data">
        <template #newsFeedButton>
          <button :class="$style.showMoreButton">Читать ленту новостей</button>
        </template>
      </PagesArticleNewsFeed>
    </div>
    <div :class="$style.main">
      <PagesArticleMain />
    </div>
    <div :class="$style.promo">
      <PagesArticlePromo />
    </div>
  </div>
</template>

<style module lang="scss">
.article {
  display: flex;
  flex-wrap: nowrap;
  gap: 20px;
  margin-left: 20px;
}
.showMoreButton {
  // empty default button styles
  background: none;
  border: none;
  padding: 0;
  margin: 0;
  font: inherit;
  cursor: pointer;

  max-width: 465px;
  color: #FFFFFF;
  width: 100%;
  height: 40px;
  font-size: 12px;
  border-radius: 50px;
  background: #0000FF;
  font-family: Cousine, serif;
  text-transform: uppercase;
  margin-top: 24px;
}
</style>
