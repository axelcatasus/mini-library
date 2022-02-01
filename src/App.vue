<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>



export default {
  data(){
    return{
      activeBook: []
    }
  },
  methods: {
    activateBook(){
      // this.activeBook = book
      console.log('HEJ')
    }
  }
}
</script>

<style lang="sass">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap')


#app
  font-family: 'Roboto', sans-serif
  max-width: 80%
  margin: 0 auto

</style>