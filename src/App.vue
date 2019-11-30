<template>
  <div id="app">
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
                <li @click="changeTab" class="nav_tab"><a href="#">Головна</a></li>
                <li @click="changeTab" class="nav_tab"><a href="#">Про нас</a></li>
                <li @click="changeTab" class="nav_tab"><a href="#">Послуги</a></li>
                <li @click="changeTab" class="nav_tab"><a href="#">Контакти</a></li>
              </ul>  
            </nav>

          <!-- this is the END burger menu  -->

        </div>
      </div>
      <div class="welcome">
        <p class="welcome__text welcome__title">Genesis Development —<br>ДНК вашого бізнесу</p>
        <p class="welcome__text welcome__subtitle">Створюємо унікальне web-обличчя для вашого проекту</p>
        <div class="welcome__wrapper">
        <button class="welcome__text welcome__button">Отримати консультацію</button>
        </div>
      </div>

  </div>
</template>

<script>

export default {
  name: 'app',
  data(){
    return{
      isTabActive: false
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
$blackColor: #020304;

@import "./assets/fonts.css";
*{
  margin: 0; 
  padding: 0; 
  box-sizing: border-box;
}
// #app {
//   font-family: 'Avenir', Helvetica, Arial, sans-serif;
//   -webkit-font-smoothing: antialiased;
//   -moz-osx-font-smoothing: grayscale;
//   text-align: center;
//   color: #2c3e50;
// }

@keyframes header-animation {
  0%{
    top: -90px;
  }
  50%{
    top: -10px;
  }
  100%{
    top: 0; 
  }
}


/* STYLES FOR HEADER  */

  .header{
    position: fixed; 
    top: -90px; 
    width: 100vw;
    height: 90px;  
    display: flex;
    background: black; 
    color: white; 
    border: solid black; 
    animation: header-animation 1s ease-in-out forwards; 
  }
  .header_left{
    width: 50%;
    display: flex; 
    justify-content: center;
    align-items: center; 
    z-index: 3;
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
    z-index: 2
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
        position: fixed;
        top: 40px;
        left: 40px;
        z-index: 0;
        font-size: 20px;
        font-weight: 900;
        font-family: sans-serif;
        text-transform: uppercase;
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
            background: white;
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
          background: black;
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
            top: 35%;
            left: 20%;
            right: 20%;
            > li {
              opacity: 0;
              transition: .5s;
              transition-delay: 0s;
              list-style-type: none;
              > a {
                text-decoration: none;
                text-transform: uppercase;
                color: white;
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

      @media (max-width: 1066px) {
        .header_right{
          padding: 0; 
        }
        .header_item_contacts{
          margin: 0; 
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
        }
        .label{
          display: block; 
        }
      }
       @media (max-width: 424px) {
        .header_item_name{
          font-size: 24px;
        }
      }
       @media (max-width: 395px) {
        .header_item_name{
          font-size: 20px;
        }
      }
      @media (max-width: 336px) {
        .header_item_name{
          font-size: 18px;
        }
        .label{
          top: 35px;
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

.welcome{
  width: 100%;
  min-height: 100vh; 
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center; 
}
.welcome__text{
  text-align: center; 
  font-family: 'Avantgard', Arial, Helvetica, sans-serif; 
  color: white; 
  margin: 20px 0; 
}
.welcome__title{
  font-size: 80px;
}
.welcome__subtitle{
  font-size: 22px;
}
.welcome__wrapper{
  width: 100%;
  text-align: center;
  margin-top: 30px;
}
.welcome__button{
  width: 200px;
  height: 44px;
  width: 320px;
  height: 54px;
  background: black; 
  border: 1px solid transparent; 
  border-radius: 30px;
  line-height: 1.55;
}

</style>