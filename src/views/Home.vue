<template>
  <div class="home">
    <h1>8 Classic Childrens books</h1><br>
    <div class="books-container">
      <Book v-for="book in this.$root.books" :key="book.Title" :book="book"></Book>
    </div>
      <button @click="$router.push( {name: 'About'} )">HEJ</button>
  </div>
</template>

<script>
import Book from '../components/Book.vue'

export default {
  components: {Book}
}
</script>

<style lang="sass">
.books-container
  display: flex
  justify-content: space-around
  flex-wrap: wrap
  

  
</style>