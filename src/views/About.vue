<template>
  <div class="about">
    <div class="back-btn">
      <router-link to="/">📚</router-link>
    </div>
  <article :class="activeBook.color" class="single-book">
		<div class="line">
			<div class="book-cover">
				<p class="author">{{activeBook.author}}</p>
				<p class="title">{{activeBook.title}}</p>  
			</div>
		</div>
  </article>
    <div class="book-info">
      <h1>{{activeBook.title}}</h1>
      <h4>By {{activeBook.author}}</h4>
      <p>{{activeBook.plot}}</p>
      <div class="book-facts">
      <p><b>Audience: </b>{{activeBook.audience}}</p>
      <p><b>First Published: </b>{{activeBook.year}}</p>
      <p><b>Pages: </b>{{activeBook.pages}}</p>
      <p><b>Publisher: </b>{{activeBook.publisher}}</p>
      </div>
    <button @click="listAdd" class="add-to-readingList">Oh, I want to read it!</button>
    </div>
  </div>
</template>


<script>
export default {
  methods: {
    listAdd(){
      if(this.$root.readingList.find(book => book == this.activeBook)){
      console.log("Den finns redan") 
      } else {
      this.$root.readingList.push(this.activeBook)
      }
    }
  },
  computed: {
    activeBook(){
      return this.$root.books.find(book => book.id == this.$route.params.id)
    }
  },
  data(){
  return{

  }
}
}

</script>

<style lang="sass" scoped>
h1
  color: white
  margin: 0

p, h4
  color: lightgray

.about
  background: black
  // height: 100vh
  width: 100vw
  display: flex
  justify-content: center
  align-items: center
  margin-top: 10rem

.back-btn
  position: absolute
  display: flex
  justify-content: center
  align-items: center
  font-size: 2rem
  top: 7rem
  left: 25.5rem
  width: 3rem
  height: 3rem
  border: 1px solid black
  border-radius: 50%
  background-color: gray

.back-btn a
  margin: 0 auto
  text-align: center
  width: 3rem
  height: 3rem

.add-to-readingList
  margin-top: 3rem
  padding: 1rem
  font-weight: 600
  border-radius: 5px
  background-color: white
  width: 200px

.book-info
  display: flex
  flex-direction: column
  justify-content: space-between
  width: 25%

.book-facts
  margin-top: 2rem
  padding: 5px
  display: grid
  grid-template-columns: 1fr 1fr
  height: 80px
  border-radius: 5px
  background: rgba(225, 225, 225, 0.1)


.book-facts p
  margin: .5rem
  line-height: 1rem

.single-book
  // display: flex
  width: 400px
  height: 480px
  color: black
  border-radius: 2px
  margin: 4rem

.single-book p
  color: black

.book-cover
  display: flex
  flex-direction: column-reverse
  justify-content: flex-start
  min-height: 100%
  min-width: 100%
  margin: 1rem

.title
  font-size: 3rem
  margin: 0

.author
  font-size: 1.5rem
  margin-top: 0rem

.line
  height: 480px
  border-left: 5px solid rgba(0,0,0,0.2)
  margin-left: 10px

.yellow
  background: linear-gradient(70deg, rgba(246, 209, 81, 1) 50%, rgba(246, 209, 81, 0.6) 100%)

.orange
  background: linear-gradient(70deg, rgba(254, 169, 100, 1) 50%, rgba(254, 169, 100, 0.6) 100%)

.red
  background: linear-gradient(70deg, rgba(254, 94, 106, 1) 50%, rgba(254, 94, 106, 0.6) 100%)

.purple
  background: linear-gradient(70deg, rgba(185, 79, 231, 1) 50%, rgba(185, 79, 231, 0.6) 100%)

.lightblue
  background: linear-gradient(70deg, rgba(92, 217, 248, 1) 50%, rgba(92, 217, 248, 0.6) 100%)

.blue
  background: linear-gradient(70deg, rgba(78, 145, 243, 1) 50%, rgba(78, 145, 243, 0.6) 100%)

.turquoise
  background: linear-gradient(70deg, rgba(110, 224, 172, 1) 50%, rgba(110, 224, 172, 0.6) 100%)

.green
  background: linear-gradient(70deg, rgba(0, 199, 129, 1) 50%, rgba(0, 199, 129, 0.6) 100%)


</style>
