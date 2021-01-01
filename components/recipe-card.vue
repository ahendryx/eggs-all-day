<template>
 <article class="card">
	 <img :src="recipe.image" :alt="recipe.name" class="card__img" width=100%>
	 <a :href="recipe.link"><h2 class="card__title">{{ recipe.name }}</h2></a>
   <p class="card__info">{{recipe.dataPoints[2].value}}</p>
 </article>
</template>


<script>
export default {
	props: {
		recipe: Object
	}
}
</script>


<style lang="scss">

@import '../assets/css/settings.variables';

.card {
	border: 2px solid $ltgray;
  max-width: 350px;
  margin: 0 0.5em 2em 0;
  color: #ccc;
  a {
    text-decoration: none;
    border: none;
    color: $dkgray;
    height: 2.2em;
    margin-left: 1em;
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
    font-size: 0.8em;
    font-style: italic;
    color: $dkgray;
    padding-top: -0.5em;
    margin-left: 1em;
  }
}

</style>
