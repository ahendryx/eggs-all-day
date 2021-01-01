<template>
 <article class="card">
	 <img :src="recipe.image" :alt="recipe.name" class="card__img">
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

.card {
	border: none;
  max-width: 300px;
  margin: 0 1em 2em 0;
	&__img {
		display: block;
		margin-bottom: 0.2rem;
	}
	&__title {
		font-size: 1.2rem;
		margin-bottom: 2rem;
	}
  &__info {
    font-size: 0.8em;
    font-style: italic;
    padding-top: 0.3em;
  }
}

</style>
