<template>
<div class="row pb-5">
  <h1 class="col-12 pt-5 pb-2">How to Cook an Egg: 4 Methods</h1>
  <p class="lead col-12 pb-5">There are a number of ways you can prepare eggs, but here we look at 4 of the most popular methods.
    And if you don’t want to cook your eggs separately, you can try one of these recipes that use raw eggs as either part of a sauce (
    <a id="content-link" href="https://www.marthastewart.com/341240/spaghetti-carbonara" target="_blank">Spaghetti Carbonara</a>,
    <a id="content-link" href="https://www.bonappetit.com/recipe/kimchi-udon-with-scallions" target="_blank">Kimchi Udon Noodles with Scallions</a>
    ) or cooks the eggs right in the dish
    <a id="content-link" href="https://www.nigella.com/recipes/eggs-in-purgatory" target="_blank">Eggs in Purgatory</a>,
    <a id="content-link" href="https://ottolenghi.co.uk/recipes/braised-eggs-with-leek-and-za-atar" target="_blank">Braised Eggs with Leek and Za'atar</a>
    ).</p>
  <section>
    <div class="cooking-method" v-for="technique in techniques" v-bind:key="technique.title">
      <image-custom :imageName="technique.img"></image-custom>

      <h3>{{technique.title}}</h3>
      <!-- Steps to method -->
      <p>{{technique.contentA}}</p>
      <p>{{technique.contentB}}</p>
      <p>{{technique.contentC}}</p>
      <!-- Link to instruction source -->
      <p class="source-link">
        <small><b>SOURCE:</b></small><br>
        <a id="content-link" :href="technique.linkA" target="_blank">{{technique.linkACopy}}</a>
      </p>

      <!-- Any additional tips or info -->
      <p>{{technique.contentD}}</p>
      <p>{{technique.contentE}}</p>
      <!-- Link for more info if needed -->
      <p><a id="content-link" :href="technique.linkB" target="_blank">{{technique.linkBCopy}}</a></p>

      <!-- 2–3 suggested recipes for this method -->
      <h4 class="pt-2 pb-3">{{technique.contentF}}</h4>
      <p><a id="content-link" :href="technique.linkC" target="_blank">{{technique.linkCCopy}}</a></p>
      <p><a id="content-link" :href="technique.linkD" target="_blank">{{technique.linkDCopy}}</a></p>
      <p><a id="content-link" :href="technique.linkE" target="_blank">{{technique.linkECopy}}</a></p>

    </div>
  </section>
</div>
</template>

<script>
import image from '../components/image.vue';

export default {

  name: 'methods',
    components: {
      'image-custom': image
    },
  data () {
    return {
      show: true,
      techniques: [
        {title: "BOILED",
          img: 'hard-boiled.jpg',
          // Use a backslash after lines of text so Javascript knows the string is continued; otherwise, errors occur
          contentA: "STEP 1: Bring a large saucepan of water to a boil over medium-high heat. Using a slotted spoon, \
          carefully lower 4–8 eggs into water one at a time. Maintaining a gentle boil, cook 10 minutes for hard-boiled eggs \
          and 6 1/2 minutes for soft-boiled. Carefully transfer eggs to a bowl of ice water and let cool until just slightly warm, \
          about 2 minutes.",
          contentB: "STEP 2: Gently crack eggs all over and peel, starting from the wider end containing the air pocket.",
          contentC: "DO AHEAD: Eggs can be cooked and peeled 3 days ahead. Transfer to an airtight container and chill.",
          linkACopy: "Bon Appetit",
          linkA: ('https://www.bonappetit.com/recipe/hard-boiled-eggs'),
          contentD: "TIP: For this method, use eggs that are a little older rather than fresh ones. This will make \
          them much easier to peel without damaging the egg white. You can see more about by visiting the link below.",
          linkBCopy: "5 Mistakes to Avoid When Making Hard-boiled Eggs",
          linkB: ('https://www.thekitchn.com/5-mistakes-to-avoid-when-making-hard-boiled-eggs-cooking-mistakes-to-avoid-216999'),
          contentF: "RECIPE SUGGESTIONS FOR THIS METHOD",
          linkCCopy: "Deviled Eggs",
          linkC: ('https://www.epicurious.com/recipes/food/views/deviled-eggs-106562'),
          linkDCopy: "Jammy Eggs with Paprika Aioli",
          linkD: ('https://www.bonappetit.com/recipe/jammy-eggs-with-paprika-aioli'),
          linkECopy: "Classic Egg Salad",
          linkE: ('https://www.marthastewart.com/314646/classic-egg-salad')
          },
          {title: "SCRAMBLED",
          img: 'scrambled.jpg',
          contentA: "STEP 1: Crack 2 eggs into a bowl and season with salt and pepper. Lightly beat with a fork until the \
          yolks and whites are combined.",
          contentB: "STEP 2: Heat a frying pan over a medium heat. Melt a teaspoon of butter in the pan, tilting and swirling \
          around so the base and most of the sides are covered. When the butter starts to foam, pour in the eggs and stir immediately \
          with a wooden spoon. Keep stirring gently as they cook to break up the egg and help it to scramble. This should \
          take 3–5 minutes.",
          contentC: "STEP 3: When the egg is nearly cooked, remove from the heat and stir in another teaspoon of butter. \
          The eggs will continue to cook in the residual heat of the pan to produce a smooth and creamy finish. Serve \
          immediately.",
          linkACopy: "BBC Food",
          linkA: ('https://www.bbc.co.uk/food/recipes/how_to_make_scrambled_93136'),
          contentF: "RECIPE SUGGESTIONS FOR THIS METHOD",
          linkCCopy: "French Omelette",
          linkC: ('https://www.thekitchn.com/how-to-make-a-french-omelette-cooking-lessons-from-the-kitchn-206018#post-recipe-9327'),
          linkDCopy: "New Mex Migas",
          linkD: ('https://www.latimes.com/recipe/new-mex-migas')
          },
          { title: "FRIED",
          img: 'overeasy.jpg',
          contentA: "STEP 1: Heat 2 tsp oil in 12- or 14-inch nonstick skillet over low heat for 5 minutes. Meanwhile, \
          crack eggs into a small bowl and season with salt and pepper.",
          contentB: "STEP 2: Increase heat to medium-high and heat until oil is shimmering. Add butter to skillet and \
          quickly swirl to coat pan. Working quickly, pour 1 bowl of eggs in 1 side of pan and second bowl of \
          eggs in other side. Cover and cook for 1 minute. Remove skillet from burner and let stand, covered, \
          15 to 45 seconds for runny yolks (white around edge of yolk will be barely opaque), 45 to 60 seconds \
          for soft but set yolks, and about 2 minutes for medium-set yolks. Slide eggs onto plates and serve.",
          linkACopy: "America's Test Kitchen (via KCET)",
          linkA: ('https://www.kcet.org/food/weekend-recipe-perfect-fried-eggs'),
          contentF: "RECIPE SUGGESTIONS FOR THIS METHOD",
          linkCCopy: "Croque Madame",
          linkC: ('https://www.marthastewart.com/353224/croque-madame'),
          linkDCopy: "Eggs in a Hole",
          linkD: ('https://www.foodnetwork.com/recipes/ree-drummond/egg-in-a-hole-recipe-1925587')
          },
          {title: "POACHED",
          img: 'poached.jpg',
          contentA: "STEP 1: Fill a medium saucepan about 2/3 full with water and bring to a boil over high heat. \
          Take the water down to a simmer. Turn the heat down and let the water relax into a brisk simmer. You should \
          see bubbles coming up to the surface, but it won't be rolling. (It's easier and quicker to control the \
          simmer if you bring it to a boil first, then reduce the heat rather than trying to get it to the perfect \
          simmer from the get-go.)",
          contentB: "STEP 2: Crack 1 large egg into a fine-mesh strainer set over a bowl. Gently swirl the egg, so \
          the thin portion of egg white is strained out. Ease the egg into the water. Make sure the water is still \
          at a bare simmer. Carefully slide the egg into the water.",
          contentC: "STEP 3: The cooking time for a poached egg is very much up to you, and it depends on how well \
          you like your eggs done and how hot the water is. But 4 minutes, give or take, in lightly simmering water, \
          will give you a firm white and a gooey but still runny yolk. Remove the egg with a slotted spoon. Use a \
          slotted spoon to remove the egg from the water.",
          linkACopy: "The Kitchn",
          linkA: ('https://www.thekitchn.com/how-to-poach-an-egg-easily-cooking-lessons-from-the-kitchn-205661'),
          contentD: "TIP: If you want to try a different method, check out Julia Child's trick for making poached eggs.",
          linkBCopy: "Julia Child's Simple Trick for Perfect Poached Eggs Every Time",
          linkB: ('https://www.thekitchn.com/julia-childs-simple-trick-for-perfect-poached-eggs-every-time-tips-from-the-kitchn-218202'),
          contentF: "RECIPE SUGGESTIONS FOR THIS METHOD",
          linkCCopy: "Frisee Salad with Warm Bacon Vinaigrette",
          linkC: ('https://www.bonappetit.com/recipe/frisee-salad-with-warm-bacon-vinaigrette?_ga=2.265406287.1149482198.1609357197-694318850.1605904741'),
          linkDCopy: "Creamy Polenta with Braised Greens and Poached Eggs",
          linkD: ('https://www.foodnetwork.com/recipes/bobby-flay/creamy-polenta-with-braised-greens-and-poached-eggs-3363887')
          }
        ],
      images: [
      {id: 1, src: require('../assets/hard-boiled.jpg'), alt:'Image of hard-boiled eggs'},
      {id: 2, src: require('../assets/scrambled.jpg'), alt:'Image of scrambled eggs'},
      {id: 3, src: require('../assets/overeasy.jpg'), alt:'Image of overeasy eggs'},
      {id: 4, src: require('../assets/poached.jpg'), alt:'Image of poached eggs'},
      ],
    }
  }
}
</script>



<style lang="scss">
@import '../assets/css/settings.variables';

section {
  display: flex;
  flex-flow: row wrap;
  .cooking-method {
    flex: 40%;
    margin: 0 2em 4em 1em;
  }
}

#content-link {
  cursor: pointer;
  font-weight: bolder;
  border: none;
  color: $dkgray;
  text-decoration: underline dotted $yellow;
}


/* Adding a media query for mobile */
@media screen and (max-width: 576px) {
  section {
    flex-flow: column wrap;
    flex: 80%;
  }
}

</style>
