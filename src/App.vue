<template>
<div id="header">
  <p class="main-text">Panel Użytkownika</p>
  <button class = "menuShow" @click = "menuSchow = !menuSchow" >Menu</button>
</div>
  <div id ="menu"  v-if = "menuSchow" >
    <div class = "menu-list">
      <ul>
        <li>
          <button class = "acc" @click="acc = !acc">Konto</button>
        </li>
        
          <li>
            <button class= "login" v-if="acc">Zaloguj się</button>
          </li>
        
          <li>
            <button class= "manage" v-if="acc">Zarządaj kontem</button>
          </li>
        
        <li>
          <button class = "news">Nowości</button>
        </li>
        
        <li>
          <button class = "orders">Zamówienia</button>
        </li>
        
        <li>
          <button class = "about">O nas</button>
        </li>
        
        <li>
          <button class = "logout">Wyloguj się</button>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>


export default {
  name: 'App',
  data () {
    return {
      acc: false,
      menuSchow: false,

    }
  }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Ubuntu&display=swap');

  body{
    font-family: 'Ubuntu', sans-serif;
    background-color: rgb(121, 121, 121);
  }
  .main-text {
    font-size: 35px;
    display: flex;
    justify-content: center;
    margin: 0px;
    padding-top: 20px;
    color: white;
  }
  #header {
    position: absolute;
    background-color: rgb(108, 98, 98);
    height: 100px;
    width:100%;
    top: 0px;
    left: 0px;
    right: 0px;
    margin: 0px;
  }
  .menuShow {
    position: absolute;
    left: 330px;
    top: 40px;
    background-color: rgb(138,138,138);
    color: white;
    width: 100px;
    height: 45px;
    display: flex;
    justify-content: center;
    font-size: 30px;
    border-radius: 25px;

  }
  #menu{
    position: absolute;
    left: 0px;
    top: 0px;
    width: 300px;
    height: 100vh;
    background-color: rgb(108, 98, 98);
    border-right-style: solid;
    border-width: 1px;
    }
  ul {
    position: absolute;
    left: 0px;
    top: 0px;
    width: 260px;
    height: 275px;
    list-style-type: none;
    
  }
    li {
      margin: 10px;
    }
      .acc, .orders, .about, .logout, .news{
        display: flex;
        justify-content: center;
        font-size: 30px;
        width: 190px;
        height: 50px;
        border-radius: 40px;
        background-color: aqua;
        margin-top: 25px;
        
      }
      .login, .manage {
        display: flex;
        justify-content: center;
        font-size: 15px;
        width: 155px;
        height: 30px;
        border-radius: 40px;
        background-color: rgba(0, 255, 255);
        margin-top: 25px;
      }
      .acc:hover, .orders:hover, .about:hover, .logout:hover, .news:hover, .login:hover, .manage:hover {
        background-color: rgba(0, 255, 255, 0.842);
      }
</style>
