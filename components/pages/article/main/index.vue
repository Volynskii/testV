<script setup lang="ts">

  const textForArticle = `
    Онлайн-опрос проводился 3-4 июля 2024 года, в нем приняли 
    участие 1500 пользователей соцсетей от 18 до 45+ лет, 
    проживающих в городах-миллионниках. 43 процента 
    опрошенных отметили, что блогеры могут повлиять на их 
    поведение — на желание попробовать новое хобби, посетить то 
    или иное место или сменить стиль одежды. В то же время 36 
    процентов россиян думают, что мнение инфлюэнсера никак не 
    влияет на их ежедневную жизнь.
  `;

  const textForFirstParagraph = 'Почти половина жителей России готова прислушиваться к мнению блогеров при выборе хобби, мест для путешествий или при смене стиля одежды. К такому выводу пришли в своем исследовании платформа коротких видео «VK Клипы» и сервис Anketolog.ru, результаты есть в распоряжении «Вести.ру».';

  const picturesData = {
    description: 'В действительности тиражируемое видео является дипфейком, о чем можно судить по ряду признаков.',
    name: 'Amir Cohen',
    position: 'Reuters'
  }


  const info = {
    created: '14:30,пн',
    updated: 'обновлено 15:02,пн',
    person: 'николай Константинопольский',
    topic: 'политика'
  };

  const dataTags = [
      {
        id: 1,
        name: 'политика'
      },
      {
        id: 2,
        name: 'вооруженные силы'
      },
      {
        id: 3,
        name: 'внутренняя политика'
      },
      {
        id: 4,
        name: 'внешняя политика'
      },
      {
        id: 5,
        name: 'политическая аналитика'
      },
      {
        id: 6,
        name: 'владимир путин'
      },
      {
        id: 7,
        name: 'иммиграция'
      },
  ];

  const infoParapraph = {
    city: 'Москва',
    date: '4 сен',
    topic: 'Вести'
  }

  const dataOtherNewsFirst = {
    title: "КПП на границе Грузии с РФ будут закрывать на три часа в день",
    time: "14:30,пн",
    image: "https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/6.jpg"
  };

  const dataOtherNewsSecond = {
    title: "КПП на границе Грузии с РФ будут закрывать на три часа в день",
    time: "14:30,пн",
    image: "https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/6.jpg"
  };

</script>

<template>
  <div :class="$style.main">

    <div :class="$style.mainPicture">
      <img :class="$style.image" src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/6.jpg" alt="main">

      <PagesArticleMainInfo 
        :created="info.created"
        :updated="info.updated"
        :person="info.person"
        :topic="info.topic"
      />
    </div>
    <div :class="$style.container">
      <div :class="$style.title">
        <h1 :class="$style.titleText">
          Путин упростил переезд в&nbsp;Россию
          из&nbsp;стран с&nbsp;&laquo;деструктивной&raquo; либеральной политикой
        </h1>
        <span :class="$style.titleInfo">
          VK Клипы: 43 % россиян считают, что блогеры могут повлиять на их стиль и хобби
        </span>
      </div>
    </div>

    <div :class="[$style.container, $style.firstParapraph]">
      <div :class="$style.firstParapraphLeft">
        <div :class="$style.infoParapraph">
          <span>{{ infoParapraph.city}}</span> · 
          <span>{{ infoParapraph.date}}</span> · 
          <span>{{ infoParapraph.topic}}</span>.
        </div>
        <PagesArticleMainParagraph :text="textForFirstParagraph"/>
      </div>

      <div :class="$style.firstParapraphRight">
        <PagesArticleMainOtherNewsMini :data="dataOtherNewsSecond" />
      </div>
    </div>

    <div :class="$style.citationBlock">
      <div :class="$style.citation">
        <div>
          <p :class="$style.text">
            Больше всего респонденты расположены
            к&nbsp;авторам по&nbsp;тематике хобби и&nbsp;увлечений&nbsp;&mdash; таким инфлюенсерам доверяют 44&nbsp;процента россиян
          </p>

          <div :class="$style.person">
            <div :class="$style.info">
              <span :class="$style.name">
                Михаил Воскресенский
              </span>
              <span :class="$style.position">
                  известный блоггер
              </span>
            </div>
            <div :class="$style.share">

            </div>
          </div>
        </div>
      </div>
    </div>

    <div :class="$style.container">
      <PagesArticleMainParagraph :text="textForArticle"/>
    </div>

    <div :class="$style.container">
      <PagesArticleMainPictures 
        :description="picturesData.description" 
        :name="picturesData.name" 
        :position="picturesData.position" 
      />
    </div>

    <div :class="$style.container">
      <PagesArticleMainParagraph :text="textForArticle"/>
    </div>

    <div :class="$style.container">
      <PagesArticleMainParagraph :text="textForArticle"/>
    </div>

    <div :class="$style.container">
      <PagesArticleMainOtherNews :data="dataOtherNewsFirst"/>
    </div>

    <div :class="$style.container">
      <PagesArticleMainParagraph :text="textForArticle"/>
    </div>

    <div :class="$style.container">
      <PagesArticleMainChanges />
    </div>

    <div :class="$style.moreNews">
      <PagesArticleMainMoreNews />
    </div>

    <div :class="$style.tags">
      <Tags :data="dataTags"/>
    </div>

    <div>
      <PagesArticleMainEmoji />
    </div>

    <div :class="$style.container">
      <PagesArticleMainSm />
    </div>

  </div>
</template>

<style module lang="scss">
  .main {
    font-family: 'NunitoSans';
    background: white;
    box-shadow: -15px 0px 20px 0px rgba(0, 0, 0, 0.3);
    padding-top: 20px;
    max-width: 645px;

    .mainPicture {
      margin-right: 21px;
      margin-bottom: 12px;

      .image {
        margin-bottom: 16px;
        width: 100%;
      }
    }

    .firstParapraph {
      display: flex;
      flex-wrap: nowrap;

      .firstParapraphLeft {
        margin-right: 16px;
      }
    }
    
    .citationBlock {
      margin: 0 28px;
      background-color: rgb(246, 238, 238);
      border-radius: 15px;
      padding: 24px;

      .citation {
        color: rgba(0, 0, 255, 1);

        .text {
          font-family: 'Manrope';
          font-size: 24px;
          font-weight: 700;
          line-height: 26.4px;
          letter-spacing: -0.05em;
          margin-bottom: 24px;
        }

        .person {
          font-family: 'Cousine';
          font-size: 12px;
          font-weight: 700;
          line-height: 16.8px;
          text-align: left;

          text-transform: uppercase;
          display: flex;

          &::before {
            content: '—';
            font-family: 'Cousine';
            font-size: 12px;
            font-weight: 400;
            line-height: 16.8px;
            margin-right: 4px;
          }

          .info {
            display: flex;
            flex-direction: column;
          }

          .name {
            font-family: 'Cousine';
            font-size: 12px;
            font-weight: 700;
            line-height: 16.8px;
            text-align: left;
          }

          .position {
          }
        }
      }
    }

    .moreNews {
      margin: 24px 27px;
    }

    .tags {
      margin: 24px 27px;
    }

    .container {
      font-family: 'Manrope';
      margin: 24px 52px 24px 52px;

      .title {
        &Text {
          font-family: 'Manrope';
          font-size: 27px;
          font-weight: 700;
          line-height: 29.7px;
          letter-spacing: -0.03em;
          text-align: left;
        }

        &Info {
          font-family: 'Cousine';
          font-size: 10px;
          font-weight: 400;
          line-height: 14px;
          letter-spacing: -0.03em;
          text-align: left;
          opacity: 0.4;
          color: rgba(0, 0, 0, 1);
          text-transform: uppercase;
        }
      }

      .infoParapraph {
        display: inline;
        font-family: 'NunitoSans';
        font-size: 17px;
        font-weight: 700;
        line-height: 22.1px;
        text-align: left;
        color: rgba(0, 0, 0, 1);
      }
    }
  }
</style>