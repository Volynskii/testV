<script setup lang="ts">
import Pppp from './sliders.vue';


</script>

<template>
  <div :class="$style.main">

    <div :class="$style.mainPicture">
      <img :class="$style.image" src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/6.jpg" alt="main">
    </div>
    <div :class="$style.container"> 
      <div :class="$style.info">
        <div :class="$style.left">
          <span :class="$style.created">14:30,пн</span>
          <span :class="$style.updated">обновлено 15:02,пн</span>
          <span :class="$style.person">/ николай Константинопольский</span>
        </div>
        <div :class="$style.right">
          <span>политика</span>
        </div>
      </div>
    </div>
    <div :class="$style.container">
      <div :class="$style.title">
        <h1>
          Путин упростил переезд в Россию
          из стран с «деструктивной» либеральной политикой
        </h1>
      </div>
    </div>

    <div :class="$style.container">
      <div :class="$style.article">
        <p>
          Почти половина жителей России готова прислушиваться к мнению блогеров при выборе хобби, мест для путешествий
          или при смене стиля одежды. К такому выводу пришли в своем исследовании платформа коротких видео «VK Клипы»
          и сервис Anketolog.ru, результаты есть в распоряжении «Вести.ру».
        </p>
      </div>
    </div>

    <div :class="$style.citationBlock">
      <div :class="$style.citation">
        <div>
          <p :class="$style.text">
            Больше всего респонденты расположены
            к авторам по тематике хобби и увлечений – таким инфлюенсерам доверяют 44 процента россиян
          </p>

          <div :class="$style.person">
            <div :class="$style.info">
              <span :class="$style.name">
                — Михаил Воскресенский
              </span>
              <span :class="$style.position">
                — известный блоггер
              </span>
            </div>
            <div :class="$style.share">

            </div>
          </div>
        </div>
      </div>
    </div>

    <div :class="$style.container">
      <div :class="$style.article">
        <p>
          Онлайн-опрос проводился 3-4 июля 2024 года, в нем приняли 
          участие 1500 пользователей соцсетей от 18 до 45+ лет, 
          проживающих в городах-миллионниках. 43 процента 
          опрошенных отметили, что блогеры могут повлиять на их 
          поведение — на желание попробовать новое хобби, посетить то 
          или иное место или сменить стиль одежды. В то же время 36 
          процентов россиян думают, что мнение инфлюэнсера никак не 
          влияет на их ежедневную жизнь.
        </p>
      </div>
    </div>

    <div :class="$style.container">
      <div :class="$style.pictures">

        <div :class="$style.picture">
          <PagesArticleMainSliders/>
        </div>
        <div :class="$style.info">
          <span>
            В действительности тиражируемое видео является дипфейком, о чем можно судить по ряду признаков. 
          </span>
          <span>
            Фото: Amir Cohen / Reuters
          </span>
        </div>
      </div>
    </div>

    <div :class="$style.container">
      <div :class="$style.article">
        <p>
          Онлайн-опрос проводился 3-4 июля 2024 года, в нем приняли 
          участие 1500 пользователей соцсетей от 18 до 45+ лет, 
          проживающих в городах-миллионниках. 43 процента 
          опрошенных отметили, что блогеры могут повлиять на их 
          поведение — на желание попробовать новое хобби, посетить то 
          или иное место или сменить стиль одежды. В то же время 36 
          процентов россиян думают, что мнение инфлюэнсера никак не 
          влияет на их ежедневную жизнь.
        </p>
      </div>
    </div>

    <div :class="$style.container">
      <div :class="$style.article">
        <p>
          Онлайн-опрос проводился 3-4 июля 2024 года, в нем приняли 
          участие 1500 пользователей соцсетей от 18 до 45+ лет, 
          проживающих в городах-миллионниках. 43 процента 
          опрошенных отметили, что блогеры могут повлиять на их 
          поведение — на желание попробовать новое хобби, посетить то 
          или иное место или сменить стиль одежды. В то же время 36 
          процентов россиян думают, что мнение инфлюэнсера никак не 
          влияет на их ежедневную жизнь.
        </p>
      </div>
    </div>

    <div :class="$style.container">
      <div :class="$style.article">
        <p>
          Онлайн-опрос проводился 3-4 июля 2024 года, в нем приняли 
          участие 1500 пользователей соцсетей от 18 до 45+ лет, 
          проживающих в городах-миллионниках. 43 процента 
          опрошенных отметили, что блогеры могут повлиять на их 
          поведение — на желание попробовать новое хобби, посетить то 
          или иное место или сменить стиль одежды. В то же время 36 
          процентов россиян думают, что мнение инфлюэнсера никак не 
          влияет на их ежедневную жизнь.
        </p>
      </div>
    </div>
    
  </div>
</template>

<style module lang="scss">
  .main {
    background: white;
    box-shadow: -15px 0px 20px 0px rgba(0, 0, 0, 0.3);
    padding-top: 20px;

    .mainPicture {
      width: 100%;
      .image {
        width: 100%;
      }
    }
    
    .citationBlock {
      margin-left: 15px;
      background-color: wheat;
      border-radius: 15px;
      padding: 24px;

      .citation {

        .text {
          margin-bottom: 24px;  
        }

        .person {
          .info {
            
          }
          .share {
            
          }
        }
      }
    }

    .container {
      font-family: 'Manrope';
      margin: 24px 32px 24px 52px;

      .title {
        font-style: normal;
        font-weight: 700;
        font-size: 20px;
        line-height: 27px;
        color: #000000;
      }

      .article {
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 22px;
        color: #000000;
      }

      .pictures {

      }

    }
  }
</style>