<template>
<div class="row pb-5">
  <h1 class="col-12 pt-5 pb-2">Recipes</h1>
  <p class="lead col-12 pb-5">Below are a few more suggestions for how to use eggs in your meals.</p>
    <section class="lead col-12 pb-5" v-if="recipes">
        <recipeCard
          v-for="recipe of recipes"
          :key="recipe.id"
          :recipe="recipe"
        />
    </section>
  <p id="credit" class="lead col-12 pb-5">CREDIT: Whisk icon by Lnhi from the <a href="https://thenounproject.com/" target="_blank">Noun Project</a></p>
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
    .get('https://api.spoonacular.com/food/site/search?query=eggs&apiKey=9993c358fa9747c1a541121a6fda81c3')
    .then(response => (this.recipes = response.data.Recipes))
    .catch(error => {
      console.log(error)
      this.errored = true
    })
    .finally(() => this.loading = false)
  },
  head() {
  return {
    title: this.title,
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Eggs are good for more than just breakfast. Get some new ideas about how to use them from this collection of recipes, with nutrition data provided.'
        }
      ]
    }
  }
}

//console.log(response)
//https://api.spoonacular.com/recipes/complexSearch?query=eggs&apiKey=35efc00cf12a4c608abe2b2839b6747e&number=10&type=mainCourse&instructionsRequired=true

</script>


<style lang="scss">
@import '../assets/css/settings.variables';

#credit {
  font-size: 0.8em;
  font-weight: 600;
  a {
    color: $dkgray;
    border: none;
    text-decoration: underline dotted $yellow;
  }
  a:hover {
    border: none;
    text-decoration: none;
  }
}

</style>
