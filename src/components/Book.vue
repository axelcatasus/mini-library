<template>
  <article>
		<p>{{book.Title}}</p>  
		<p>{{book.Author}}</p>  
  </article>
</template>

<script>
export default {
	props: {book: Object},
	computed: {
		bookColor() {
			return this.colors[Math.floor(Math.random(this.colors.length))]
		}
	},
	data(){return {
		colors: ['yellow', 'orange', 'red', 'purple', 'lightblue', 'blue', 'turqouise', 'green']
	}}
}
</script>

<style lang="sass">

article
	margin: 1rem
	background: linear-gradient(45deg, rgba(0, 0, 0, .5), white)
	border: 1px black solid
	width: 200px
	height: 240px

p
	margin: 2rem

.yellow
	background-color: yellow

.orange
	background-color: orange
</style> 