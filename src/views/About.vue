<template>
  <div class="about">
    <router-link to="/">Home</router-link>
  </div>
</template>
<script>
export default {
	props: {book: Object},
  data(){
  return{
    readingList: [],
  }
}
}

</script>
