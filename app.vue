<template>
  <div>
    <NuxtLayout name="common">
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<style lang="scss">
  @font-face {
    font-family: 'Manrope';
    src: url('@/assets/fonts/Manrope/Manrope-VariableFont_wght.ttf') format('truetype');
  }

  @font-face {
    font-family: 'Cousine';
    src: url('@/assets/fonts/Cousine/Cousine-Regular.ttf') format('truetype'),
        url('@/assets/fonts/Cousine/Cousine-Bold.ttf') format('truetype'),
        url('@/assets/fonts/Cousine/Cousine-BoldItalic.ttf') format('truetype'),
        url('@/assets/fonts/Cousine/Cousine-Italic.ttf') format('truetype');
    font-style: normal, bold, italic, normal italic;
    font-weight: 400, 700;
  }

  @font-face {
    font-family: 'NunitoSans';
    src: url('@/assets/fonts/NunitoSans/NunitoSans-VariableFont_YTLC,opsz,wdth,wght.ttf') format('truetype');
  }

  * {
    box-sizing: border-box;
  }

  body {
    font-family: 'Manrope', sans-serif;
    background: black;
    display: flex;
    justify-content: center;
  }
  
</style>