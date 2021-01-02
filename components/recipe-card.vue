<template>
 <article class="card">
	 <img :src="recipe.image" :alt="recipe.name" class="card__img" width=100%>
	 <a :href="recipe.link" target="_blank"><h2 class="card__title">{{ recipe.name }}</h2></a>
    <div class="card__info">
      <p v-if="show">Click the whisk to preview nutrition information.</p>
      <p v-else>{{recipe.dataPoints[1].value + ', ' + recipe.dataPoints[2].value + ', ' +
         recipe.dataPoints[3].value + ', ' + recipe.dataPoints[4].value}}</p>
      <button id="nutrition-info" v-on:click="show = !show" v-bind:key="msg" type="button"><img class="icon" src="../assets/whisk-icon.svg" alt="whisk" width=45%></button>
    </div>
 </article>
</template>


<script>

export default {
	props: {
		recipe: Object
	},
  data () {
      return {
        show: true
      }
  }
}
</script>


<style lang="scss">

@import '../assets/css/settings.variables';

.card {
	border: 2px solid $ltgray;
  background-color: #fff;
  max-width: 300px;
  margin: 0 0.5em 2em 0;
  a {
    text-decoration: none;
    border: none;
    color: $dkgray;
    height: 2.2em;
    margin-left: 0.5em;
  }
  a:hover {
    color: $yellow;
    background-color: none;
    box-shadow: none;
  }
	&__img {
		margin-bottom: 0.1rem;
	}
	&__title {
		font-size: 1.2rem;
		margin-bottom: 2rem;
	}
  &__info {
    font-size: 0.7em;
    color: $dkgray;
    margin-left: 0.7em;
    padding-top: 0.3em;
    }
  #nutrition-info {
    width: 20%;
    border: none;
    outline: none;
    background-color: #fff;
    padding: 0.5em 0 1em 0;
  }
  .icon {
    margin-left: -2em;
  }
  .icon:hover {
    transform: rotate(0.25turn);
  }
  .icon:visited {
    opacity: 0.5;
  }
  .icon:active {
    opacity: 0.25;
  }
}

</style>
