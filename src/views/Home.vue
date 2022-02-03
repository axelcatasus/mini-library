<template>
  <div class="home">
    <h1>8 Classic Childrens books</h1><br>
    <div class="books-container">
        <router-link v-for="book in this.$root.books" :key="book.title" :to="'/books/'+book.id">
          <Book :book="book"></Book>
        </router-link>
    </div>
  </div>
</template>

<script>
import Book from '../components/Book.vue'

export default {
  components: {Book},
  computed: {
  fixedPath(book){
    return book.title.replace(/\s+/g, '-')
    },
  },
  data(){
    return{
      
    }
  },
}
</script>

<style lang="sass">
.books-container
  width: 60%
  margin: 0 auto
  // display: flex
  // justify-content: space-around
  // flex-wrap: wrap
  display: grid
  grid-template-columns: repeat(4,1fr)
  column-gap: 0
  row-gap: 1rem
  
</style>