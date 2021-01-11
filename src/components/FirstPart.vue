<template>
  <div class="BG-image">
    <div class="wrapper col-12 col-sm-6 col-md-4 col-xl-3">
      
      <div class="header ">
  
        <div class="navigation col-12 col-sm-6 col-md-4 col-xl-3">
          <img src="../assets/LogoRU.png" alt="">
  
         <div class="links" style="color: #333333;">
          <a class="link" href="#">Купить полис</a>
          <a class="link" href="#"> Продукты </a>
          <a class="link" href="#">О компании</a>
          <a class="link" href="#">Страховой случай</a>
          <a class="link" href="#">Партнёрам</a>
          <a class="link" href="#">Контакты </a>
          <button class="Agent"><a href="#">Вход для агентов </a></button>
         </div>
        </div>
        <div class="container">
          <div class="main_text">
            <h1>Страховка для путишествий в Египет</h1>
          </div>
          <div class="lite">
            <p>Рассчитать и оформить туристическую страховку<sup>*</sup></p>
  
          </div>
          <Cards></Cards>
        </div>
      </div>
    </div>
  </div>
  </template>
  
  <script>
  import Cards from './cards'
  export default {
    components: {
      Cards
    }
  }
  </script>
  
  <style>
    .BG-image 
    {
    position: relative;
    width: 100%;
    height: 1080px;
    background-image: url('../assets/01.png');
    background-size: 100% 100%;
    }
    .wrapper {
      display: flex;
      justify-content: center;
      width: 1200px;
      margin: 0 auto;
    }
    .header {
      height: 80px;
      background:rgba(255, 255, 255, 0.95);
      box-shadow: 0px 4px 8px rgba(0,0,0,0.2);
    }
    .main_text {
      display: flex;
      justify-content: flex-start;
      margin-top: 190px;
    }
    .container {
      margin-left: 40px;
    }
    .main_text h1 {
      font-size: 60px;
      line-height: 72px;
      }

    h1, p {
      color: white;   
       }
    p {
      font-size: 32px;
    }
    .navigation {
      display: flex;
      justify-content: space-between;
      padding-right: 32px;
      margin: 0;
  
    }
    .links {
      padding-top: 15px;
      color: #333333;

    }
    .link {
      font-size: 14px;
      line-height: 20px;
      letter-spacing: 0.015em;
      padding-right: 15px;
      padding-bottom: 10px;
    }
    .link:active {
      border-bottom: 2px solid #BEB400;
      color: #A0A0A0;
    }
    a {
      text-decoration: none;
    }
    .Agent {
      padding: 10px 12px;
      border: 1px solid #78A7CD;
      box-sizing: border-box;
      border-radius: 4px;
    }


@media  (max-width: 700px) {
  .header {
    width: 100%;
    margin: 0;
  }
  .container {
    margin-right: 44%;  }
  .main_text {
    margin-top: 50px;
  }
}
  </style>
  