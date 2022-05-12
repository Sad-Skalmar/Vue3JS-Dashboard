<template>
  <div id ="menu">
    <div class = "small-title">Menu</div>
    <div class = "menu-list" >
      <ul>
        <li class = "acc" @click="acc = !acc">Konto</li>
          <li class= "login" v-if="acc">Zaloguj się</li>
          <li class= "manage" v-if="acc">Zarządaj kontem</li>
          <li class= "manage" v-if="acc">Ustawienia Konta</li>
        <li class = "orders">Zamówienia</li>
        <li class = "about">O nas</li>
        <li class = "logout">Wyloguj się</li>
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

    }
  }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Ubuntu&display=swap');

  body{
    font-family: 'Ubuntu', sans-serif;
  }
  #menu{
    width: 200px;
    height: 500px;
    border-radius: 40px;
    background-color: red;
    }
  ul {
    position: fixed;
    left: 20px;
    background-color: darkgray;
    width: 250px;
    height: 275px;
    
  }
    li {
      margin: 10px;
    }
      .acc{
        display: flex;
        justify-content: center;
        font-size: 30px;
        width: 185px;
        height: 45px;
        border-radius: 40px;
        background-color: aqua;
       
        margin-top: 25px;
      }
      .orders{
        display: flex;
        justify-content: center;
        font-size: 30px;
        width: 185px;
        height: 50px;
        border-radius: 40px;
        background-color: aqua;
       
      }
      .about {
        display: flex;
        justify-content: center;
        font-size: 30px;
        width: 185px;
        height: 50px;
        border-radius: 40px;
        background-color: aqua;
       
      }
      .logout {
        display: flex;
        justify-content: center;
        font-size: 30px;
        width: 185px;
        height: 50px;
        border-radius: 40px;
        background-color: aqua;
      }
</style>
