<template>
  <article :class="book.color">
		<div class="line">
			<div class="book-cover">
				<p class="author">{{book.author}}</p>
				<p class="title">{{book.title}}</p>  
			</div>
		</div>
  </article>
</template>

<script>


export default {
	props: {book: Object},
	methods: {
		activateBook(){
			// this.$root.activeBook = this.book
			// this.$router.push( {name: 'About'} )
			// this.$emit('BookClick', this.book)
	// 		if(this.activeBook.length){
    //     this.activeBook = []
    //     this.activeBook.push(this.book)
    //     console.log(this.activeBook)
    //   }else{
    //     this.activeBook.push(this.book)
    //     console.log(this.activeBook)
		
		}
	},
	computed: {
		fixedPath(){
			return this.book.title.replace(/\s+/g, '-')
		},
	},
	data(){return {
	}}
}
</script>

<style lang="sass" scoped>

article
	// margin: 1rem
	// background: linear-gradient(45deg, rgba(0, 0, 0, .5), white)
	width: 200px
	height: 240px
	// display: flex
	// flex-direction: column
	// justify-content: flex-end
	color: white
	border-radius: 2px
	box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px

.line
	height: 240px
	border-left: 3px solid rgba(0,0,0,0.2)
	margin-left: 5px

.book-cover
	width: 180px
	height: 240px
	margin-left: 10px
	display: flex
	flex-direction: column-reverse
	// justify-content: flex-end

.title
	// font-weight: bold
	font-size: 1.2rem
	margin: 0 0 0 .4rem

.author
	font-size: .6rem
	margin: 0 0 .4rem .4rem

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