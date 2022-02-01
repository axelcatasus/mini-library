<template>
  <div class="home">
    <h1>8 Classic Childrens books</h1><br>
    <div class="books-container">
      <Book v-for="book in this.$root.books" :key="book.Title" :book="book"></Book>
    </div>
  </div>
</template>

<script>
import Book from '../components/Book.vue'

export default {
  components: {Book},
  data(){
    return{
    }
  },
}
</script>

<style lang="sass">
.books-container
  max-width: 80%
  display: flex
  justify-content: space-around
  flex-wrap: wrap
  

  
</style>