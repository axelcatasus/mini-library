<template>
  <div class="about">
    <div class="back-btn">
      <router-link to="/">B</router-link>
    </div>
  <article :class="book.Color" class="">
		<div class="line">
			<div class="book-cover">
				<p class="author">{{activeBook.Author}}</p>
				<p class="title">{{activeBook.Title}}</p>  
			</div>
		</div>
  </article>
    <div class="book-info">
      <h1>{{this.$root.activeBook.Title}}</h1>
      <h4>{{this.$root.activeBook.Author}}</h4>
      <p>{{this.$root.activeBook.Plot}}</p>
      <div class="book-facts">
      <p><b>Audience: </b>{{this.$root.activeBook.Audience}}</p>
      <p><b>First Published: </b>{{this.$root.activeBook.Year}}</p>
      <p><b>Pages: </b>{{this.$root.activeBook.Pages}}</p>
      <p><b>Publisher: </b>{{this.$root.activeBook.Publisher}}</p>
      </div>
    <button class="add-to-readingList">Oh, I want to read it!</button>
    </div>
  </div>
</template>

<script>
export default {
  data(){
  return{
    readingList: [],
  }
}
}

</script>

<style lang="sass" scoped>
.about
  display: flex
  justify-content: center
  align-items: center

.back-btn
  width: 1rem
  border: 1px solid black
  border-radius: 2rem
  background-color: gray

.add-to-readingList
  padding: 1rem
  font-weight: 600
  border-radius: 5px
  background-color: white
  width: 200px

.book-facts
  display: flex
  flex-direction: row
  flex-wrap: wrap
  width: 400px
  height: 80px
  border: 1px solid black
  border-radius: 5px

.single-book
  width: 400px
  height: 480px
  color: black

.line
  height: 480px


</style>
