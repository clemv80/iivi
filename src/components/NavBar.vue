<template>
  <div id="navbar">
    <img id="logo" :src="image">
    <p>Je suis une barre de navigation</p>
  </div>
</template>

<script>
import logo from '../assets/logo.png'
export default {
  data () {
    return {
      image: logo
    }
  }
}
</script>

<style scoped>
  #navbar {
    position: fixed;
    width: 100%;
    height: 50px;
    left: 0px;
    top: 0px;
    background-color: #DDDDDD;
  }
  #logo {
    width: 40px;
    height: 40px;
    margin-left: 5px;
    margin-top: 5px;
  }
</style>
