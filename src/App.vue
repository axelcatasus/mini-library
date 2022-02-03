<template>
  <div id="app">
    <div id="nav">
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

:root
  background: black
  padding: 0

a
  text-decoration: none
  width: 0rem

#app
  font-family: 'Roboto', sans-serif
  // max-width: 80%
  // margin: 0 auto

</style>