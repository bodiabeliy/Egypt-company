<template>
<v-app>
  <div class="v-wrapper">
    <FirstPart></FirstPart>
    <div class="health_polic">
      <div class="wrapper">
        <div class="heder_text">
          <h1 class="headering" style="color: #333333;">Все ок, вы застрахованы.</h1>
          <div class="polic_cards">
            <div v-for="item in items" :key="item.key" class="polic_card">
              <img class="image" src="../src/assets/pulse.svg" alt="">
              <h1 style="color: #333333; font-size: 20px; line-height: 24px;;"><b>{{item.title}}</b></h1>
              <p style="color: #333333;  font-size: 20px; line-height: 24px;">{{item.description_text}}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="offers">
      <div class="wrapper">
        <div class="main_content">
          <div class="offer_container_one">
            <div class="map">
              <div class="text_map">
                <h1 class="color" style="font-size: 32px;">Сосредоточьтесь на путешествии</h1>
                <p class="color" style="font-size: 18px;">
                 {{map_text_p1}}
                </p>
                <ul class="color">
                  <li>амбулаторное истационарное лечение;</li>
                  <li>экстренная стоматология;</li>
                  <li>медико-транспортные расходы;</li>
                  <li style="padding-top: 16px;">поисково спасательные мероприятия (включая спасательный вертолет)</li>
                  <p class="color" style="font-size: 18px;"><b>…и многое другое.</b></p>
                </ul>
                <p class="color" style="font-size: 18px;">
                  При оформлении полиса покажем весь перечень. покрываемых рисков и вы егко выберите продходящую программу.
                </p>
              </div>
              <div class="img_map">
                <img src="../src/assets/lupa.png" alt="">
              </div>
            </div>
            <div class="bike">
              <div class="bike_img" style="margin-right: 112px;">
                <img src="../src/assets/bikewoman.png" alt="">
              </div>
              <div class="bike_text">
                <h1 class="color" style="font-size: 32px;">Активный отдых</h1>
                <p class="color" style="font-size: 18px;">
                 {{bike_text_p1}}
                </p>
                <ul class="color">
                  <li>{{list1}}</li>
                  <li>{{list2}}</li>
                  <li style="padding-bottom: 16px;">{{list3}}</li>
                </ul>
                <p class="color" style="font-size: 18px;">
                 <b> {{bike}}</b>
                </p>
              </div>
            </div>
            <div class="extrim">
             <div class="text-extrim">
              <h1 class="color" style="font-size: 32px;">Спортивный и экстремальный отдых</h1>
              <p class="color" style="font-size: 18px;">Любите горнолыжные склоны? Или исследования морских глубин? Без проблем, ведь у ERV есть страховки и для такого отдыха</p>
              <p class="color" style="font-size: 18px;">Прыжки с парашютом, полеты на дельтаплане или параплане, альпинизм, участие в соревнованиях, кстати, тоже можно застраховать.</p>
             </div>
             <div class="extrim_img" style="margin-left: 112px;">
              <img src="../src/assets/daiver.png" alt="">
            </div>
          </div>
          <div class="Covid">
            <div class="Covid_img" style="margin-right: 112px;">
              <img src="../src/assets/Virus.png" alt="">
            </div>
            <div class="Covid_text">
              <h1 class="color" style="font-size: 32px; padding-top: 52px;">COVID-19 уже встраховке</h1>
              <p class="color" style="font-size: 18px;">{{Covid}}</p>
            </div>
          </div>
        </div>
        </div>
      </div>
      <div class="ERV">
        <div class="overlay"></div>
      </div>
    </div>
  </div>
</v-app>
</template>

<script>
import FirstPart from './components/FirstPart'
export default {
  components: {
    FirstPart
  },
  data: () => ({
    items: [
      {image:'../src/assets/medical-threatment-icon.svg', hey: 1,  title:'Амбулаторное и стационарное лечение', description_text:'Возместим расходы на посещение врача или лечение в стационаре'},
      {image: '../src/assets/hospitalization-icon.svg', hey: 2, title:'Хронические заболевания', description_text:'Экстренная помощь при обострении хронических заболеваний, аллергии и солнечных ожогах.'},
      {image: '../src/assets/Infation.svg', hey: 3, title:'Опасные инфекции', description_text:'Оплатим лечение при коронавирусной инфекции, а также проживание в случае задержки в поездке из-за каранитнного заболевания'},
      {image: '../src/assets/pulse.svg', hey: 4, title:'Лекарства по рецепту', description_text:'Если врач пропишет лекарства, то мы возместим расходы на их приобретение'},
    ],
    map_text_p1: 'Все программы ERV устроены так, чтобы вы могли спокойно путешествовать не думая о страховке. Чтобы вы были уверены, мы предусмотрели основные риски:',
    bike_text_p1: 'Необязательно все время лежать на пляже. Поэтому во всех программах ERV, по умолчанию, без переплат и оговорок, покрывается активный отдых:',
    list1: 'активности на море и/или бассейне, пляжные развлечения, развлечения в отелях, парках, аттракционы;',
    list2: 'пешие прогулки, катание на беговых лыжах, экскурсии, походы, в т. ч. с участием животных;',
    list3: 'передвижения в качестве пассажира, экскурсанта на самолетах, яхтах, катерах, лодках, автомобилях и пр.;',
    bike:'И еще множество активностей и развлечений. Не ограничивайте себя!',
    Covid:'Заболевание коронавирусом покрываем в любой программе ERV. Оплатим консультации врачей, лечение в больнице, анализы, а также медико-транспортные расходы. И все это — в пределах страховой суммы.'
  })
}
</script>
<style>
  .v-wrapper {
    width: 1920px;
    height: 2150px;
    background:#e3e3e3;
    font-family: 'Anonymous Pro', monospace;
  }
  .color {
    color: #333333;
  }
  .wrapper {
      display: flex;
      justify-content: center;
      width: 1200px;
      margin: 0 auto;
    }
  .health_polic {
      height: 604px;
      background: #FFFFFF;
    }
    .heder_text {
      width: 100%;
      padding-top: 128px;
      color: #333333;
    }
    .polic_cards {
      margin-top: 60px;
      position: relative;
      display: flex;
      justify-content: space-around;
    }
    .polic_card {
      width: 240px;
    }
    .offers {
      width: 100%;
      height: 2064px;
      background: #F4F4F4;
    }
    .offers_continue {
      width: 100%;
      height: 1488px;
      background: white;
    }
    .main_content {
      display: flex;
      flex-direction: column;
      padding-top: 128px;
      padding-bottom: 128px;
    }
    .map {
      display: flex;
      justify-content: center;
      margin-bottom: 128px;
    }
    .text_map {
      max-width: 560px;
    }
    .bike {
      display: flex;
      justify-content: center;
      margin-bottom: 128px;
    }
    .bike_text {
      max-width: 560px;
    }
    .extrim {
      display: flex;
      justify-content: center;
      margin-bottom: 128px;
    }
    .text-extrim {
      max-width: 560px;
    }
    .Covid {
      display: flex;
      justify-content: flex-start;
    }
    .Covid_text {
      max-width: 560px;
    }
    .ERV {
      position: relative;
      opacity: 1;
      width: 100%;
      height: 1080px;
      background-image: url('../src/assets/ERV.png');
      background-size: 100% 100%;
      }
      .overlay {
        background: rgba(34, 56, 128, 0.68);
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
      }

  @media  (max-width: 700px) {
    .health_polic {
      height: 1500px;
    }
   .headering {
     text-align: center;
     font-size: 90px;
   }
   .polic_cards {
    display: flex;
    flex-direction: column;
   }
   .polic_card {
     padding: 30px;
     margin: 15px;
     width: 100%;
     box-shadow:0 0 8px 0 #9e9d9d;   
     border-radius: 3%;
     text-align: center;
     }
     .bike img {
      margin-left: 152px
     }
     .Covid img{
      margin-left: 112px
     }
     .map, .bike, .extrim, .Covid {
       flex-direction: row-reverse;
     }
     .image {
       width: 100px;
     }
     

}
@media  (max-width: 1000px) {
  .health_polic {
      height: 1500px;
    }
   .polic_cards {
    display: flex;
    flex-direction: column;
   }
   .polic_card {
     padding: 50px;
     margin: 15px;
     width: 100%;
     border-radius: 3%;
     text-align: center;
     }
}
</style>
