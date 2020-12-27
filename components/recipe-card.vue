<template>
 <article class="card">
	 <img :src="recipe.image" :alt="recipe.name" class="card__img">
	 <h2 class="card__title">{{ recipe.title }}</h2>
	<!-- <a :href="url">{{ recipe.sourceUrl }}</a> -->
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
	margin: 1rem;
	border: 1px solid #000;
	padding: 1.5rem;
	max-width: 200px;
	min-height: 200px;
	&__img {
		display: block;
		margin-bottom: 1rem;
	}
	&__title {
		font-size: 1rem;
		margin-bottom: .25rem;
	}
	&__copy {
		font-size: .875rem;
	}
}
</style>
