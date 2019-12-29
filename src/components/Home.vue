<template>
  <div id="home">
    <h1 v-if="visible">Bienvenue</h1>
    <h2>Bonjour {{ user.name }}</h2>
    <p>Voici mon message : {{ message }}</p>
    <p>Voici le premier mot : {{ onlyFirstWord }}</p>
    <button v-on:click="btnClick">{{ i }}</button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      user: {
        name: 'Clément',
        city: 'Amiens'
      },
      visible: true,
      i: 0
    }
  },
  computed: {
    onlyFirstWord () {
      return this.message.split(' ')[0].toUpperCase()
    },
    message () {
      return this.user.city + ' c\'est cool !'
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
  #home {
    text-align: center;
  }
</style>
