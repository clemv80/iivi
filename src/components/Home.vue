<template>
  <div>
    <img :src="image">
    <h1 v-if="visible">Bienvenue</h1>
    <h2>Bonjour {{ user }}</h2>
    <p>Voici mon message : {{ message }}</p>
    <p>Voici le premier mot : {{ onlyFirstWord }}</p>
    <button v-on:click="btnClick">{{ i }}</button>
  </div>
</template>

<script>
import logo from '../assets/logo.png'
export default {
  data () {
    return {
      user: 'Clément',
      visible: true,
      message: 'Hello world.',
      image: logo,
      i: 0
    }
  },
  computed: {
    onlyFirstWord () {
      return this.message.split(' ')[0].toUpperCase()
    }
  },
  methods: {
    btnClick () {
      this.i += 1
      return this.i
    }
  }
}
</script>

<style scoped>

</style>
