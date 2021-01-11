<template>
<div class="cards" >
  <div class="chose_country">
    <div class="text_field">
  <v-text-field
  class="col-sm-12 col-sm-6 col-md-12"
  @keypress="Calculation"
  v-model="city"
  outlined
  clearable
  background-color="white"
  hint="Список доступных городов: Каир Лукос Хургада Дахаб"
  >
  </v-text-field>
  <div class="range_of_time">
    <v-text-field class="df" 
    v-model="dateFirst"
    outlined
    clearable
    background-color="white"
    label="Туда"
    ></v-text-field>
   <div class="colum_button">
    <button @click="showF" class="first"><i class="fal fa-calendar-edit"></i></button>
    <button  @click="showL" class="last"><i class="fad fa-calendar-edit"></i></button>
   </div>
    <v-text-field class="df" 
    v-model="dateLast"
    outlined
    clearable
    background-color="white"
    label="Обратно"
    ></v-text-field>
  </div>
  <div class="description">
    <h1 style="font-size: 12px;"><sup>*</sup>Страховой полис оформляется на период кратный году. Максимальный период - 5 лет</h1>
  </div>
  <div class="priceTotalBtn">
    <h1 class="pricing">{{price  + ' Грн.'}}</h1>
    <button @click="Calculation" class="TotalPrice"><h1 class="linkheder">Купить онлайн</h1></button>
  </div>

    <div class="wrapper-calendar" style="display: flex; justify-content: space-between;">
      <v-date-picker v-model="dateFirst" timezone="timezone" is-range class="dateFist" />
      <v-date-picker v-model="dateLast" timezone="timezone" is-range class="dataLast"/>
    </div>
    
    </div>
  </div>
  <div class="course">
    <div class="text_info">
      <p style="color: #BEB400;font-size: 15px;line-height: 16px;">Валюта</p>
      <p style="font-size: 20px;line-height: 24px;">Египетский фунт (EGP) <br> ≈ 5 ₽ </p>
      <p style="color: #BEB400;font-size: 15px;line-height: 16px; margin: 0;">Виза</p>
      <p style="font-size: 20px;line-height: 24px;">Не нужна</p>
      <p style="color: #BEB400;font-size: 15px; margin: 0;">Красота пирамид</p>
      <v-rating
      empty-icon="far fa-star"
      full-icon="fas fa-star"
      length="5"
      size="14"
      background-color="grey lighten-2"
      color="#dde008"
    ></v-rating>

    </div>
  </div>
  <div class="banner">
   <img src="../assets/banner.png" alt="">
  </div>
</div>
</template>

<script>
 export default {
  data:() => ({
    city: '',
    dateFirst: '',
    dateLast: '',
    timezone: '',
    visible: false,
    price: 500
}),
methods: {
  showF () {
    var show = document.querySelector('.dateFist')
    show.classList.toggle('dateFistVisible')
  },
  showL () {
    var show = document.querySelector('.dataLast')
    show.classList.toggle('dateLastisible')
  },
  Calculation () {
    var FirstDate = parseInt(this.dateFirst)
    var LastDate = parseInt(this.dateLast)
    let result = LastDate - FirstDate
    console.log(result)
    if (this.city  === 'Каир' ) {
      this.price = 1500
      if (result === 0) {
        this.price +=2000
        this.co
      }
      if (result === 1) {
        this.price +=3500
      }
      if (result === 2) {
        this.price +=5000
      }
      if (result === 3) {
        this.price +=8000
      }
      if (result === 4) {
        this.price +=12000
      }
      if (result === 5) {
        this.price +=15000
      }
    }
    if (this.city  === 'Лукос' ) {
      this.price = 900
      if (result === 0) {
        this.price +=1100
      }
      if (result === 1) {
        this.price +=2450
      }
      if (result === 2) {
        this.price +=3800
      }
      if (result === 3) {
        this.price +=5500
      }
      if (result === 4) {
        this.price +=8000
      }
      if (result === 5) {
        this.price +=10000
      }
    }
    if (this.city  === 'Хургада' ) {
      this.price = 1200
      if (result === 0) {
        this.price +=1700
      }
      if (result === 1) {
        this.price +=3000
      }
      if (result === 2) {
        this.price +=4800
      }
      if (result === 3) {
        this.price +=7500
      }
      if (result === 4) {
        this.price +=9400
      }
      if (result === 5) {
        this.price +=12500
      }
    }
    if (this.city  === 'Дахаб' ) {
      this.price = 1000
      if (result === 0) {
        this.price +=1300
        this.co
      }
      if (result === 1) {
        this.price +=2700
      }
      if (result === 2) {
        this.price +=4000
      }
      if (result === 3) {
        this.price +=6100
      }
      if (result === 4) {
        this.price +=8700
      }
      if (result === 5) {
        this.price +=11300
      }
    }
  }
}
};
</script>

<style>
.description {
  padding-bottom: 10px;
}
.dateFist, .dataLast {
  margin-top: 20px;
  position: absolute;
  opacity: 0;
}
.dataLast {
margin-left: 30px;
}

.dateFistVisible, .dateLastisible {
  opacity: 1;
}

.cards {
 display: flex;
 justify-content: flex-start;
 margin-top: 59px;
 width: 1200px;
}
.chose_country {
 width: 464px;
 height: 308px;
 background: rgba(13,13,13, 0.5);
 margin-right: 112px;
}
.course {
 width: 176px;
 height: 285px;
 background: rgba(13,13,13, 0.5);
 margin-right: 112px;
}
.banner {
 margin-top: 140px;
}
.range_of_time {
  display: flex;
  justify-content: space-between;
  height: 55px;
}
.text_field {
  padding-top: 36px;
  margin-left: 24px;
  margin-right: 24px;
  margin-bottom: 24px;
}
.colum_button {
  display: flex;
}
.first, .last {
  width: 50px;
  height: 55px;
  background:  #BEB400;
  border: 1px solid white
}
.first {
  margin-right: 15px;
}
.first:hover, .last:hover {

  background:  #696404;
  border: 1px solid rgb(114, 109, 109)
}

.df {

  margin-left: 20px;
  width: 200px;
}
.priceTotalBtn {
  display: flex;
  justify-content: space-between;
}
.TotalPrice {
  width: 189px;
  height: 56px;
  background: #BEB400;
  border-radius: 4px;
  padding: 16px 28px;
}
.TotalPrice:hover {
  background:  #696404;
}
.linkheder {
  font-size: 18px;
}
.text_info {
  padding-top: 20px;
  margin-left: 16px;
}

@media  (max-width: 700px) {
 .cards {
   width: 100%;
   display: flex;
   flex-direction: column;
 }
 .course {
   display: none;
 }
 .chose_country {
   width: 100%;
   margin-top: 0px;
   height: 400px;
 }
 .description {
   margin-top: 45px;
 }
 .priceTotalBtn {
   margin-top: 20px;
   justify-content: space-around;
 }
 .TotalPrice {
   width: 30%;
 }
 .pricing {
   font-size: 60px;
 }
 .banner {
   padding-bottom: 170px;
   display: flex;
   justify-content: center;
   transform: scale(1.4);
 }
 .wrapper-calendar {
   justify-content: space-between;
 }
}
</style>