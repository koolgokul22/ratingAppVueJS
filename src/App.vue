<template>
<div class="container">
  <div class="card card-body text-center p-5 mt-5 border-primary">
    <div class="mb-5 mt-2"><h1 id="title">Rating App</h1></div>
    <div id="stars">
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

@import url('https://fonts.googleapis.com/css2?family=Fuzzy+Bubbles:wght@400;700&display=swap');

body {
  background: linear-gradient(0.25turn, #3f87a6, #ebf8e1, #f69d3c);
  font-family: 'Fuzzy Bubbles', cursive;
}

#title{
  font-size: 5rem;
  font-weight: 800;
  /* text-shadow: 2px 3px rgb(168, 165, 165); */
}

#title:hover{
  text-shadow: 2px 3px rgb(255, 255, 255);
}

.card{
  background: linear-gradient(217deg, rgba(255,0,0,.1), rgba(255,0,0,0) 70.71%),
            linear-gradient(127deg, rgba(69, 75, 69, 0.1), rgba(0,255,0,0) 70.71%),
            linear-gradient(336deg, rgba(0,0,255,.1), rgba(0,0,255,0) 70.71%);
          
  border: none;
  box-shadow: 5px 10px rgba(83, 75, 75, 0.452);
  
}

div i {
  cursor: pointer;
  border-radius: 20%;
  background: rgb(145, 74, 192);
  padding: 0.5rem;
  box-shadow: 5px 10px rgb(93, 57, 119);
  margin: 0.5rem;
}

#stars{
  border-radius: 20%;
  padding: .5rem;
}

div>i:hover {
  background: rgba(182, 29, 54, 0.925);
  /* cursor: pointer; */
  border-radius: 20%;
  /* padding: 1rem; */
  transform: scale(1.10);
  box-shadow: 5px 10px rgb(136, 39, 39);
}


</style>
