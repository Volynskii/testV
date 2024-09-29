
<script setup lang="ts">

</script>

<template>
  <div :class="$style.article">
      <PagesArticleNewsFeed />
      
      <PagesArticleMain />
      
      <PagesArticlePromo />
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