
<script setup lang="ts">

</script>

<template>
  <div :class="$style.article">
    <div :class="$style.newsFeed">
      <PagesArticleNewsFeed />
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
</style>