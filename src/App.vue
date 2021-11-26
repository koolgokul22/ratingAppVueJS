<template>
<div class="container">
  <div class="card card-body text-center p-5 mt-5 border-primary">
    <div class="mb-5 mt-2"><h1>Rating App</h1></div>
    <div>
      <i class="fa fa-star text-warning fa-6x" @click="setRating(1)"></i>
      <i class="fa fa-star text-warning fa-6x" @click="setRating(2)"></i>
      <i class="fa fa-star text-warning fa-6x" @click="setRating(3)"></i>
      <i class="fa fa-star text-warning fa-6x" @click="setRating(4)"></i>
      <i class="fa fa-star text-warning fa-6x" @click="setRating(5)"></i>
    </div>
    <h1 class="text-sucess mt-4" v-if="rating == 1">Hmm! Sorry to hear that rating</h1>
    <h1 class="text-sucess mt-4" v-if="rating == 2">We'll certainly improve your experience next time</h1>
    <h1 class="text-sucess mt-4" v-if="rating == 3">Alright! Three stars !</h1>
    <h1 class="text-sucess mt-4" v-if="rating == 4">Good! 4 stars</h1>
    <h1 class="text-sucess mt-4" v-if="rating == 5">Wohoo!! A Five star rating!</h1>
  </div>
</div>
  
</template>


<script>
export default {
  name: 'App',
  data(){
    return {
      rating: null,
      star: 'warning' 
    }
  },
  methods:{
    setRating(rating){
      this.rating = rating
      this.star = 'success'
    },
    changeColor(){
      this.star = 'success'

    }
  }
}
</script>


<style>
body {
  background-color: #333
}

</style>
