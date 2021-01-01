<template>
<div class="row pb-5">
  <h1 class="col-12 pt-5 pb-2">Recipes</h1>
  <p class="lead col-12 pb-5">Below are a few more ideas for how to use eggs in your meals.</p>
    <section class="container" v-if="recipes">
        <recipeCard
          v-for="recipe of recipes"
          :key="recipe.id"
          :recipe="recipe"
        />
    </section>
</div>
</template>


<script>
import axios from 'axios';
import recipeCard from '../components/recipe-card.vue';

export default {
  components: {
    recipeCard
  },
  data() {
    return {
      loading: true,
      recipes: null,
      errored: false
    }
  },
  mounted () {
  axios
    .get('https://api.spoonacular.com/food/site/search?query=egg&apiKey=9993c358fa9747c1a541121a6fda81c3')
    .then(response => (this.recipes = response.data.Recipes))
    .catch(error => {
      console.log(error)
      this.errored = true
    })
    .finally(() => this.loading = false)
  }
}

//console.log(response)
//https://api.spoonacular.com/recipes/complexSearch?query=eggs&apiKey=35efc00cf12a4c608abe2b2839b6747e&number=10&type=mainCourse&instructionsRequired=true


</script>
