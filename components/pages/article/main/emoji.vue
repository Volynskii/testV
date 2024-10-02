<script setup lang="ts">
  import emoji1 from '@/assets/images/emoji/like.svg';
  import emoji2 from '@/assets/images/emoji/dislike.svg';
  import emoji3 from '@/assets/images/emoji/smile.svg';
  import emoji4 from '@/assets/images/emoji/surprised.svg';
  import emoji5 from '@/assets/images/emoji/sad.svg';
  import emoji6 from '@/assets/images/emoji/angry.svg';

  const emoji = [
    {
      img: emoji1,
      name: 'like',
      vote: 12
    },
    {
      img: emoji2,
      name: 'dislike',
      vote: 1
    },
    {
      img: emoji3,
      name: 'smile',
      vote: 3
    },
    {
      img: emoji4,
      name: 'surprised',
      vote: 23
    },
    {
      img: emoji5,
      name: 'sad',
      vote: 5
    },
    {
      img: emoji6,
      name: 'angry',
      vote: 1

    },
  ];

</script>

<template>
  <div :class="$style.emoji">
    <div :class="$style.item" v-for="(item, index) in emoji" :key="item.name">
      <img :src="item.img" :alt="item.name" :aria-label="item.name">
      <span :class="$style.vote">{{ item.vote }}</span>
    </div>
  </div>
</template>

<style module lang="scss">
.emoji {
  display: flex;
  flex-wrap: nowrap;
  justify-content: center;

  .item {
    width: 70px;
    height: 60px;
    border-radius: 60px;
    background: rgba(245, 245, 245, 1);

    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  .vote {
    font-family: 'Manrope';
    font-size: 12px;
    font-weight: 600;
    line-height: 13.92px;
    text-align: left;
  }
}
</style>