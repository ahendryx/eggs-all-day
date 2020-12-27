<template>
<div>
  <h1>Recipes</h1>
  <p class="intro-secondary">Below are a few more ideas for how to use eggs in your meals.</p>
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
import RecipeCard from '../components/recipe-card.vue';

export default {
  components: {
    RecipeCard
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
    .get('https://api.spoonacular.com/recipes/complexSearch?apiKey=35efc00cf12a4c608abe2b2839b6747e&query=eggs&type=mainCourse&number=2&includeInstruction=true')
    .then(response => (this.recipes = response.data))
    .catch(error => {
      console.log(error)
      this.errored = true
    })
    .finally(() => this.loading = false)
  }
}

</script>
