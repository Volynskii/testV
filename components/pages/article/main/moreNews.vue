<script setup lang="ts">

</script>

<template>
  <div :class="$style.moreNews">
    
    <div :class="$style.earlier">
      <div>
        <span :class="$style.title">Ранее</span>
        <p :class="$style.description">
          VK Клипы — самая популярная российская платформа коротких вертикальных видео, по данным Mediascope. В апреле 2024 года среднесуточное количество зрителей «VK Клипов» превысило
          33 миллиона человек.
        </p>
      </div>
    </div>
    
    <div :class="$style.readAlso">
      <div>
        <span :class="$style.title">Читайте также</span>

        <div :class="$style.readAlsoList">
          <div :class="$style.readAlsoItem">
            <div :class="$style.readAlsoItemTop">
              <p>
                Маск после интервью
                с Трампом заявил, что готов взять интервью
                у Харрис 
              </p>
            </div>
            <div :class="$style.readAlsoItemBottom">
              <span :class="$style.time">13:45</span>
              <div :class="$style.picture"><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/6.jpg" alt=""></div>
            </div>
          </div>
          <div :class="$style.readAlsoItem">
            <div :class="$style.readAlsoItemTop">
              <p>
                Маск после интервью
                с Трампом заявил, что готов взять интервью
                у Харрис 
              </p>
            </div>
            <div :class="$style.readAlsoItemBottom">
              <span :class="$style.time">13:45</span>
              <div :class="$style.picture"><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/6.jpg" alt=""></div>
            </div>
          </div>
          <div :class="$style.readAlsoItem">
            <div :class="$style.readAlsoItemTop">
              <p>
                Маск после интервью
                с Трампом заявил, что готов взять интервью
                у Харрис 
              </p>
            </div>
            <div :class="$style.readAlsoItemBottom">
              <span :class="$style.time">13:45</span>
              <div :class="$style.picture"><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/6.jpg" alt=""></div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<style module lang="scss">
  .moreNews {
    padding: 24px 21px 20px 21px;
    background: hwb(300 87% 13%);
    border-radius: 20px;
    display: flex;
    flex-direction: column;
    gap: 40px;

    .title {
      display: block;
      font-family: 'Cousine';
      font-size: 12px;
      font-weight: 700;
      line-height: 16.8px;
      text-align: left;
      margin-bottom: 16px;
      text-transform: uppercase;
    }

    .earlier {
      .description {
        font-family: 'NunitoSans';
        font-size: 17px;
        font-weight: 400;
        line-height: 22.1px;
        letter-spacing: -0.03em;
        text-align: left;
      }
    }

    .readAlso {

      &List {
        display: flex;
      }

      &Item {
        margin-right: 20px;
        position: relative;

        &::after {
          content: '';
          position: absolute;
          top: 0px;
          right: 0px;
          height: 100%;
          width: 1px;
          background: rgb(200, 200, 203);
          z-index: 0;
        }

        &Top {
          p {
            font-size: 14px;
            font-weight: 600;
            line-height: 16.24px;
            text-align: left;
            color: rgba(20, 22, 26, 1);
            margin: 0 16px 8px 0;
          }
        }

        &Bottom {

          display: flex;
          flex-wrap: nowrap;
          justify-content: space-between;
          align-items: end;
          position: relative;
          z-index: 1;

          .time {
            font-family: 'Cousine';
            font-size: 10px;
            font-weight: 400;
            line-height: 12px;
            letter-spacing: 0.06em;
            text-align: left;
            
          }

          .picture {
            width: 80px;
            height: 50px;

            img {
              width: 100%;
              height: 100%;
            }
          }
        }
      }
    }
  }
</style>