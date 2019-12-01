<template>
  <div id="app">
  <!-- HEADER  -->
      <div class="header">
        <div class="header_left">
          <p class="header_item header_item_name">GENESIS DEVELOPMENT</p>
        </div>
        <div class="header_right">
          <p class="header_item header_item_main">Головна</p>
          <p class="header_item header_item_about">Про нас</p>
          <p class="header_item header_item_service">Послуги</p>
          <p class="header_item header_item_contacts">Контакти</p>

          <!-- this is burger menu  -->

            <input id="burger" type="checkbox" v-model="isTabActive">
            <label class="label" for="burger">
                <span></span>
                <span></span>
                <span></span>
            </label>
            
            <nav>    
              <ul>
                <li @click="changeTab" class="nav_tab"><a class="nav_tab_item" href="#">Головна</a></li>
                <li @click="changeTab" class="nav_tab"><a class="nav_tab_item" href="#">Про нас</a></li>
                <li @click="changeTab" class="nav_tab"><a class="nav_tab_item" href="#">Послуги</a></li>
                <li @click="changeTab" class="nav_tab"><a class="nav_tab_item" href="#">Контакти</a></li>
              </ul>  
            </nav>

          <!-- this is the END burger menu  -->

        </div>
      </div>
  <!-- THE END OF HEADER  -->

<!-- FIRST WELCOME BLOCK  -->

      <div style="overflow: hidden;" class="welcome">
        <p class="welcome__text welcome__title">Genesis Development —<br>ДНК вашого бізнесу</p>
        <p class="welcome__text welcome__subtitle">Створюємо унікальне web-обличчя для вашого проекту</p>
        <div class="welcome__wrapper">
          <button class="welcome__text welcome__button">Отримати консультацію</button>
        </div>
      </div>

<!-- THE END OF FIRST WELCOME BLOCK  -->

<!-- SECOND BLOCK  -->

    <div class="goodsBlock">
            <h3 class="goodsBlockTitle">Розробляємо складні та нестандартні сайти, сервіси та мобільні додатки</h3>
            <div class="goodsImage">
              <div class="good" v-for="(good,i) in goods" :key="i">
                <div class="goodContainer">
                  <div class="goodImageContainer">
                    <img :src="good.img" alt="" class="goodImage">
                  </div>
                  <p class="goodText">{{good.txt}}</p>
                </div>
              </div>
            </div>
    </div>

<!-- END OF THE SECOND BLOCK  -->

<!-- THIRD BLOCK ABOUT MAIN TARGET OF GENESIS -->
  <div class="target">
    <div class="target_left">
      <div class="target_left_container">
        <img src="./assets/images/target.svg" alt="image">
      </div>
    </div>
    <div class="target_right">
      <p class="target_right_text">ЗВЕРТАЮЧИСЬ ДО<br>НАС, ВИ ОТРИМУЄТЕ<br>РІШЕННЯ<br>МАРКЕТИНГОВИХ І<br>БІЗНЕС-ЗАДАЧ:<br>ФІНАНСОВИХ ТА<br>НЕФІНАНСОВИХ</p>
    </div>
  </div>
<!-- THE END OF THIRD BLOCK ABOUT MAIN TARGET OF GENESIS -->


<!-- FOURTH BLOCK WITH ALL STEPS THAT PROVIDE GENESIS COMPANY  -->
    <div class="steps">
      <h2 class="steps_title">Для цього ми проведемо вас по всіх<br>етапах створення кращого веб-продукту:</h2>
      <div class="steps_schema">
        <div class="steps_schema_picture">
          <div class="line">
            <div class="steps_schema_picture_element"></div>
            <div class="steps_schema_picture_element"></div>
            <div class="steps_schema_picture_element"></div>
            <div class="steps_schema_picture_element"></div>
          </div>
            <div class="steps_schema_card steps_schema_card_first">
              <img class="card_image" src="./assets/images/third1.svg" alt="card's image">
              <p class="card_title">Дизайн Мислення</p>
              <p class="card_text">Знаємо, як у короткі терміни<br>вивести новий продукт на ринок</p>
            </div>
            <div class="steps_schema_card steps_schema_card_second">
              <img class="card_image" src="./assets/images/third2.svg" alt="card's image">
              <p class="card_title">Технічна Стратегія</p>
              <p class="card_text">Розбираємо вашу технічну задачу<br>та підбираємо оптимальний стек<br>технологій</p>
            </div>
            <div class="steps_schema_card steps_schema_card_third">
              <img class="card_image" src="./assets/images/third3.svg" alt="card's image">
              <p class="card_title">UX Аудит</p>
              <p class="card_text">Аналізуємо шлях клієнта та досвід<br>його взаємодії з вами, усуваємо<br>слабкі місця</p>
            </div>
            <div class="steps_schema_card steps_schema_card_fourth">
              <img class="card_image" src="./assets/images/third4.svg" alt="card's image">
              <p class="card_title">Тестування Якості</p>
              <p class="card_text">Допоможемо знайти всі баги та<br>недоліки в продукті перед його<br>запуском</p>
            </div>
        </div>

      </div>
    </div>

<!-- THE END OF FOURTH BLOCK WITH ALL STEPS THAT PROVIDE GENESIS COMPANY  -->



  </div>
</template>

<script>
import img1 from './assets/images/1-01.svg'
import img2 from './assets/images/1-02.svg'
import img3 from './assets/images/1-03.svg'
import img4 from './assets/images/1-04.svg'
import img5 from './assets/images/1-05.svg'
import img6 from './assets/images/1-06.svg'
import img7 from './assets/images/1-07.svg'
import img8 from './assets/images/1-08.svg'
import img9 from './assets/images/1-09.svg'

export default {
  name: 'app',
  data(){
    return{
      isTabActive: false,
      goods: [
          {
            img: img4,
            txt: 'Фінансові проекти'
          },
          {
            img: img2,
            txt: 'Криптовалютні біржі'
          },
          {
            img: img7,
            txt: 'Корпоративні додатки'
          },
          {
            img: img1,
            txt: 'Портали нерухомості'
          },
          {
            img: img6,
            txt: 'Новинні портали'
          },
          {
            img: img3,
            txt: 'Інтернет-магазини'
          },
          {
            img: img8,
            txt: 'Дошки оголошень'
          },
          {
            img: img9,
            txt: 'Сервіси знайомств'
          },
          {
            img: img5,
            txt: 'Соціальні мережі'
          }
        ]
    }
  }, 
  methods:{
    changeTab(){
      this.isTabActive = !this.isTabActive;
    }
  }
}
</script>

<style lang="scss" >
$blackColor: #000000;;

@import "./assets/fonts.css";
*{
  margin: 0; 
  padding: 0; 
  box-sizing: border-box;
}
body{
  max-width: 100vw; 
}
// ALL ANIMATIONS

    @keyframes header-animation {
      0%{
        top: -90px;
      }
      100%{
        top: 0; 
      }
    }
    @keyframes header-items {
      0%{
        margin-top: -110px;
      }
      100%{
        margin-top: 0px;
      }
    }
    @keyframes welcome-title{
      0%{
        opacity: 0;
        margin-left: -100%;
      }
      100%{
        opacity: 1;
        margin-left: 0;
      }
    }
    @keyframes welcome-subtitle{
      0%{
        top: 150%;
        opacity: 0;
      }
      100%{
        top: 57.7%;
        opacity: 1;
      }
    }
    @keyframes welcome-button{
      0%{
        top: 150%;
        opacity: 0;
      }
      100%{
        top: 67%;
        opacity: 1;
      }
    }
// THE END OF ANIMATION'S LIST   

/* STYLES FOR HEADER  */

  .header{
    position: fixed; 
    top: -90px; 
    width: 100vw;
    height: 90px;  
    display: flex;
    background:  #000000;; 
    color: #ffffff;; 
    border: solid  #000000;; 
    animation: header-animation 1s  ease-out forwards; 
    z-index: 9999;
  }
  .header_left{
    width: 50%;
    display: flex; 
    justify-content: center;
    align-items: center;
    z-index: 3;
    margin-top: -110px;
    animation: header-items 1s ease-out forwards;
  }
  .header_item{
    margin-right: 35px;
    font-family: 'Avantgard', Arial, Helvetica, sans-serif; 
    font-size: 17px; 
    font-weight: 700;
  }
  .header_item_name{
    font-family: 'Avantgard', Arial, Helvetica, sans-serif; 
    font-size: 26px; 
    font-weight: 900;
    margin: 0;
    margin-left: 27px;
  }
  .header_right{
    width: 50%; 
    display: flex; 
    justify-content: center;
    align-items: center;
    padding-right: 10%;
    z-index: 2;
    margin-top: -110px;
    animation: header-items 1s ease-out forwards;
  }

  // THE BURGER STYLING 

      #burger{
        visibility: hidden;
        display: none;
      }
      .label{
        display: none;
      }
      body {
      background-color: #ed5050;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      h1 {
        > span {
          text-transform: none;
          opacity: .5;
          font-weight: 300;
          font-size: 12px;
        }
      }
        input + label {
          position: fixed;
          top: 35px;
          right: 40px;
          height: 20px;
          width: 15px; 
          z-index: 2;
          span {
            position: absolute;
            width: 100%;
            height: 2px;
            top: 50%;
            margin-top: -1px;
            left: 0;
            display: block;
            background: #ffffff;;
            transition: .5s;
          }
          span:first-child {
            top: 3px; 
          }
          span:last-child {
            top: 16px; 
          }      
        }
        label:hover {
          cursor: pointer;
        }
        input:checked + label { 
          span {
            opacity: 0;
            top: 50%;
          }
          span:first-child {
            opacity: 1;
            transform: rotate(405deg);
          }
          span:last-child {
            opacity: 1;
            transform: rotate(-405deg);
          }
        }
        input ~ nav {
          background:  #000000;;
          position: fixed;
          top: 0px;
          left: 0;
          width: 100%;
          height: 0px;
          z-index: 1;
          transition: .5s;
          transition-delay: .5s;
          overflow: hidden;
          > ul {
            text-align: center;
            position: absolute;
            // top: 35%;
            // left: 20%;
            // right: 20%;
                margin: auto;
                top: 0;
                bottom: 0;
                left: 0;
                right: 0;
                height: fit-content;
            > li {
              opacity: 0;
              transition: .5s;
              transition-delay: 0s;
              list-style-type: none;
              > a {
                text-decoration: none;
                text-transform: uppercase;
                color: #ffffff;;
                font-family: 'Avantgard', Arial, Helvetica, sans-serif; 
                font-size: 17px; 
                font-weight: 700;
                font-weight: 700;
                display: block;
                padding: 30px;
              }
            }
          }
        }
        input:checked ~ nav { 
          height: 100%;
          transition-delay: 0s;
          > ul {
            > li {
              opacity: 1;
              transition-delay: .5s;
            }
          }
        }
    }

  // END OF THE BURGER STYLING 

  /* header media requirements    */
      @media (max-height: 400px) {
        .header{
          height: 70px;
        }
        .header_left{
          justify-content: flex-start;
        }
        .welcome{
          padding-top: 70px;
        }
      }

      @media (max-width: 1066px) {
        .header_right{
          padding: 0; 
        }
        .header_item_contacts{
          margin: 0; 
        }
        .nav_tab_item{
          padding: 15px;
        }
      }
       @media (max-width: 840px) {
        .header_item{
          display: none; 
        }
        .header_item_name{
          display: block; 
        }
        .header_right{
          width: 25%;
        }
        .header_left{
          width: 75%;
          justify-content: flex-start; 
        }
        .label{
          display: block; 
        }
      }
       @media (max-width: 424px) {
        .header_item_name{
          font-size: 20px;
        }
         .label{
          top: 36px;
        }
      }
       @media (max-width: 395px) {
        .header_item_name{
          font-size: 20px;
        }
      }
      @media (max-width: 336px) {
        .header{
           height: 70px;
         }
        .welcome{
          padding: 70px 0;
        }
        .header_item_name{
          font-size: 18px;
        }
        .label{
          top: 26px;
        }
      }
       @media (max-width: 307px) {
         .header{
           height: 70px;
         }
        .header_item_name{
          font-size: 16px;
        }
        .label{
          top: 26px;
        }
      }
         /* @media (max-width: 368px) {
        .header_item_name{
          font-size: 12px;
        }
      } */

/*END OF STYLES FOR HEADER  */

// STYLES FOR FIRST WELCOME BLOCK 

  .welcome{
    width: 100%;
    height: 100vh;
    min-height: 277px; 
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center; 
    overflow: hidden;
  }
  .welcome__text{
    text-align: center; 
    font-family: 'SF', Arial, Helvetica, sans-serif; 
    color: #ffffff;; 
    margin: 20px 0; 
  }
  .welcome__title{
    font-family: 'Avantgard', Arial, Helvetica, sans-serif; 
    font-size: 80px;
    margin-left: -10400px;
    opacity: 0;
    animation: welcome-title 1s ease-out forwards;
    line-height: 1.1;
    margin-bottom: 138px;
  }
  .welcome__subtitle{
    font-size: 22px;
    font-weight: 300; 
    position: absolute; 
    margin: auto;
    left: 0; 
    right: 0; 
    top: -150%;
    animation: welcome-subtitle 1s ease-in-out forwards;
  }
  .welcome__wrapper{
    width: 100%;
    text-align: center;
    position: absolute; 
    margin: auto;
    left: 0; 
    right: 0; 
    top: 150%;
    animation: welcome-button 1.1s ease-in-out forwards;
  }
  .welcome__button{
    width: 17%;
    min-width: 230px;
    height: 54px;
    padding: 0 20px;
    background:  #000000;; 
    border: 1px solid transparent; 
    border-radius: 30px;
    line-height: 1.55;
    font-weight: 300; 
    font-size: 17px;
  }

  // media requirements of welcome block 
  @media (max-width: 1030px) {
        .welcome__title{
          font-size: 80px; 
        }
        .welcome__subtitle{
          font-size: 22px; 
        }
        .welcome__button{
          font-size: 17px; 
        }
  }
  @media (max-width: 980px) {
        .welcome__title{
          font-size: 60px; 
        }
        .welcome__subtitle{
          font-size: 17px; 
        }
        .welcome__button{
          font-size: 17px; 
        }
  }
  @media (max-width: 745px) {
        .welcome__title{
          font-size: 50px; 
        }
        .welcome__subtitle{
          font-size: 15px; 
        }
        .welcome__button{
          font-size: 12px; 
        }
  }
  @media (max-width: 630px) {
        .welcome__title{
          font-size: 40px; 
        }
        .welcome__subtitle{
          font-size: 14px; 
        }
        .welcome__button{
          font-size: 12px; 
        }
  }
  @media (max-width: 510px) {
        .welcome__title{
          font-size: 30px; 
          margin-bottom: 20%;
        }
        .welcome__subtitle{
          width: 187px;
          font-size: 14px; 
        }
        .welcome__button{
          font-size: 12px; 
        }
  }
  @media (max-width: 370px) {
        .welcome__title{
          font-size: 25px; 
          margin: 0; 
          display: block;
          margin-top: 30%;
        }
        .welcome__subtitle{
          font-size: 12px; 
          position: static; 
          animation: none; 
          display: block;
          margin: 20px auto;
        }
        .welcome__wrapper{
          position: static; 
          animation: none; 
          display: block;
          margin: 0 auto 20px auto;
        }
        .welcome__button{
          font-size: 12px; 
          margin: 0;
        }
  }
  @media (max-width: 337px) {
    .welcome__title{
          font-size: 20px; 
          width: 100%;
        }
  }
      // for iPad Pro 

        @media only screen 
          and (min-width: 1024px) 
          and (max-height: 1366px) 
          and (-webkit-min-device-pixel-ratio: 1.5) {
            .welcome__title{
              font-size: 77px; 
              width: 100%;
            }
            .welcome__subtitle{
              font-size: 29px;
              // margin-top: -65px; 
            }
            .welcome__button{
              font-size: 27px; 
              min-width: 40%;
              max-width: 40%; 
              height: 76px;
              border-radius: 50px;
              margin: 0;
            }
        }

        /* Portrait */
        @media only screen 
          and (min-width: 1024px) 
          and (max-height: 1366px) 
          and (orientation: portrait) 
          and (-webkit-min-device-pixel-ratio: 1.5) {

        }

        /* Landscape */
        @media only screen 
          and (min-width: 1024px) 
          and (max-height: 1366px) 
          and (orientation: landscape) 
          and (-webkit-min-device-pixel-ratio: 1.5) {
            
        }

      // end requirements for iPad Pro 


  // END OF media requirements of welcome block 


//END OF STYLES FOR FIRST WELCOME BLOCK 

// STYLING FOR SECOND BLOCK 

    .goodsBlock {
      display: flex;
      flex-direction: column;
      text-align: center;
      align-content: center;
      align-items: center;
    }
    .goodsBlockTitle {
      font-family: 'Avantgard', Arial, Helvetica, sans-serif;
      font-size: 42px;
      color: #fff;
      margin-bottom: 90px;
      max-width: 940px;
      width: 80%;
    }
    .goodsImage {
      display: flex;
      flex-wrap: wrap;
      width: 80%;
      max-width: 1199px;
      justify-content: space-between;
    }
    .goodContainer {
      width: 300px;
    }
    .good {
      display: flex;
      flex-direction: column;
      max-width: 300px;
      margin-bottom: 120px;
    }
    .goodImageContainer {
      height: 200px;
    }
    .goodText {
      font-family: 'Avantgard', Arial, Helvetica, sans-serif;
      font-size: 20px;
      color: #fff;
    }
    .goodImage {
      width: 160px;
    }

    // media requirements second block 

      @media screen and (max-width: 1140px) {
        .goodsImage {
          flex-direction: column;
          justify-content: center;
          align-items: center;
        }
        .good {
          margin-bottom: 60px;
        }
        .goodContainer{
          width: fit-content;
        }
      }
      @media (max-width: 945px){
        .goodsBlockTitle{
          font-size: 33px
        }
      }
      @media (max-width: 745px){
        .goodsBlockTitle{
          margin: 0;
          margin: 50px 0 30px 0;
          font-size: 30px;
        }
        .goodText{
          font-size: 23px;
        }
      }
      @media (max-width: 589px){
        .goodsBlockTitle{
          font-size: 26px;
        }
        .goodText{
          font-size: 23px;
        }
      }
      @media (max-width: 400px){
        .goodsBlockTitle{
          font-size: 23px;
        }
        .goodText{
          font-size: 23px;
        }
      }

    // END OF THE media requirements second block 


// END OF STYLING FOR SECOND BLOCK 


// STYLES FOR THIRD BLOCK 

.target{ 
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
  height: 100vh;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  align-items: center;
}
.target_left{
  width: 560px;
  height: 560px;
  max-width: 560px;
  max-height: 560px;
  box-shadow: 0px 0px 15px 0px rgba(0, 0, 0, 0.20);
}
.target_right{
  width: 560px;
  height: 560px; 
  display: flex;
  flex-direction: column;
  justify-content: center; 
  align-content: flex-start; 
}
.target_right_text{
    color: #ffffff;
    font-size: 42px; 
    font-family: 'Avantgard', Arial, Helvetica, sans-serif; 
    font-weight: 900; 
}

    // MEDIA REQUIREMENTS FOR THIRD BLOCK 
      @media (max-width: 1300px){
        .target{
          max-width: 985px;
          min-width: 985px;
        }
        .target_left{
          width: 460px;
          height: 460px;
        }
        .target_right {
          width: 460px;
          height: 460px;
            }
      }
       @media (max-width: 1050px){
        .target{
          max-width: fit-content;
          min-width: fit-content;
          height: fit-content;
          flex-direction: column;
          align-items: center;
        }
        .target_left{
          width: 600px;
          height: 600px;
        }
        .target_right {
          width: 100vw;
          text-align: center;
        }
      }
      @media (max-width: 1200px){
        .target_left{
          width: 460px;
          height: 460px;
        }
      }
       @media (max-width: 491px){
        .target_left{
          width: 90%;
          height: auto;
        }
        .target_right{
          height: fit-content;
          margin-top: 10%;
        }
        .target_right_text{
          font-size: 30px;
        }
      }
      @media (max-width: 330px){
        .target_right_text{
          font-size: 24px;
        }
      }

    // THE END MEDIA REQUIREMENTS FOR THIRD BLOCK 
    

// THE END OF STYLES FOR THIRD BLOCK 


// STYLES FOR FOURTH BLOCK 

  .steps{
    height: fit-content;
    width: 100%; 
  }
  .steps_title{
    width: 100%;
    height: fit-content;
    font-size: 45px;
    color: #ffffff;;
    font-family: 'Avantgard';
    font-weight: bold; 
    text-align: center;
    margin: 100px 0;
  }
    .steps_schema_picture{
      height: 1262px;
      position: relative; 
      display: flex; 
      flex-direction: column; 
      justify-content: center;
      align-items: center; 
    }
  // styling for picture of checkpiont line 

    .line{
      height: 830px;
      width: 0; 
      background: #ffffff;
      border: 1px solid #ffffff;
      position: absolute;
      margin: auto;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0; 
      display: flex; 
      flex-direction: column; 
      justify-content: space-between;
      align-items: center;
    }
    .steps_schema_picture_element{
        height: 25px;
        width: 25px;
        border: 5px solid #ffffff;; 
        border-radius: 50%;
        background: #000000;
    }
    .steps_schema_picture_element:first-child{
      margin-top: -3px;
    }
    .steps_schema_picture_element:last-child{
      margin-bottom: -3px;
    }

  // End styling for picture of checkpiont line 


  // styles for cards 
    .card_title{
      font-size: 29px;
      font-family: 'Avantgard';
      font-weight: bold;
      color: #ffffff; 
      width: 100%;
      height: fit-content;
      margin: 10px 0; 
    }
    .card_text{
      font-size: 15px;
      font-family: 'SF',Arial,sans-serif;
      line-height: 1.55;
      font-weight: 600;
      color: #000000; 
    }
    .steps_schema .steps_schema_card .card_image{
      width: 120px;
      height: 120px;
    }
    .steps_schema_card{
      width: 272px;
      height: fit-content;
      text-align: center;
      position: absolute;
      margin: auto; 
      top: 0;
      right: 0;
      bottom: 0;
      left: 0; 
    }
    .steps_schema_card:nth-child(2n){
      align-self: flex-end;
    }
    .steps_schema_card_first{
      margin-top: 0px;
      top: 71px;
      right: 400px;
    }
    .steps_schema_card_second{
       margin-top: 0px;
       left: 400px;
       top: 343px;
    }
    .steps_schema_card_third{
      margin-top: 0px;
      right: 400px;
      top: 611px;
    }
    .steps_schema_card_fourth{
      margin-top: 0px;
         left: 400px;
      top: 883px; 
    }

  // THE END  of styles for cards 

    // media requirements of third block 

      @media (max-width: 945px){
        .steps_title{
          margin: 50px 0 30px 0;
          font-size: 33px
        }
      }
      @media (max-width: 745px){
        .steps_title{
          margin: 50px 0 30px 0;
          font-size: 30px
        }
        .steps_schema_picture{
          position: static;
        }
        .line{
          display: none;
        }
        .steps_schema_card{
          position: static;
          margin: 0; 
          margin: 30px 0; 
        }
        .steps_schema_card:nth-child(2n){
          align-self: center;
        }
      }
      @media (max-width: 685px){
        .steps_title{
          font-size: 28px;
        }
      }
      @media (max-width: 625px){
        .steps_title{
          font-size: 26px;
          width: 80%;
          margin: 0 auto;
          margin-top: 50px;
        }
      }
      @media (max-width: 400px){
        .steps_title{
          font-size: 23px;
        }
        .card_title{
          font-size: 23px;
        }
      }

    // media requirements of third block 

// THE END OF STYLES FOR FOURTH BLOCK 

</style>