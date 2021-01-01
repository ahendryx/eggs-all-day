<template>
<div class="row pb-5">
  <h1 class="col-12 pt-5 pb-2">How to Cook an Egg: 4 Methods</h1>
  <p class="lead col-12 pb-5">There are a number of ways you can cook eggs, but here we look at 4 of the most popular methods.
    Don’t want to cook your eggs separately? Try one of these recipes that use raw eggs as either part of a sauce
    (Spaghetti Carbonara, Kimchi Noodles), or cook the eggs right in a sauce (Eggs in Purgatory*, Green Shakshuka).
    <!-- * Shortcut: Skip making your own tomato sauce and use a good jarred sauce. Rao’s Arrabiata is my personal favorite. --></p>
  <section>
    <div class="cooking-method" v-for="technique in techniques" v-bind:key="technique.title">
      <image-custom :imageName="technique.img"></image-custom>

      <h3>{{technique.title}}</h3>
      <!-- Steps to method -->
      <p>{{technique.contentA}}</p>
      <p>{{technique.contentB}}</p>
      <p>{{technique.contentC}}</p>
      <!-- Link to instruction source -->
      <p>
        <small><b>SOURCE:</b></small><br>
        <a id="content-link" :href="technique.linkA" onclick="_blank">{{technique.linkACopy}}</a>
      </p>

      <!-- Any additional tips or info -->
      <p>{{technique.contentD}}</p>
      <p>{{technique.contentE}}</p>
      <!-- Link for more info if needed -->
      <p><a id="content-link" :href="technique.linkB">{{technique.linkBCopy}}</a></p>

      <!-- Three suggested recipes for this method -->
      <h4>{{technique.contentF}}</h4>
      <p><a id="content-link" :href="technique.linkC">{{technique.linkCCopy}}</a></p>
      <p><a id="content-link" :href="technique.linkD">{{technique.linkDCopy}}</a></p>
      <p><a id="content-link" :href="technique.linkE">{{technique.linkECopy}}</a></p>

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
          linkA: ('https://www.bbc.co.uk/food/recipes/how_to_make_scrambled_93136'),
          contentF: "RECIPE SUGGESTIONS FOR THIS METHOD",
          linkC: ('https://www.thekitchn.com/how-to-make-a-french-omelette-cooking-lessons-from-the-kitchn-206018#post-recipe-9327'),
          linkD: ('https://www.latimes.com/recipe/new-mex-migas'),
          linkE: ('https://www.marthastewart.com/314646/classic-egg-salad')
          },
          { title: "FRIED",
          img: 'overeasy.jpg',
          contentA: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod \
          tempor incididunt ut labore et dolore magna aliqua. In egestas erat imperdiet sed euismod.\
          Maecenas sed enim ut sem viverra aliquet eget sit amet. Libero volutpat sed cras ornare \
          arcu dui vivamus arcu. Egestas sed sed risus pretium quam vulputate dignissim. Leo urna \
          molestie at elementum eu facilisis sed. In aliquam sem fringilla ut morbi tincidunt augue. \
          Egestas diam in arcu cursus euismod quis viverra. Ut eu sem integer vitae. Arcu ac tortor \
          dignissim convallis aenean. At elementum eu facilisis sed odio morbi quis commodo. \
          Fringilla ut morbi tincidunt augue interdum velit euismod. Aliquam ultrices sagittis orci \
          a scelerisque purus semper eget duis.",
          contentB: "Sit amet luctus venenatis lectus magna fringilla urna porttitor. Habitasse \
          platea dictumst quisque sagittis purus sit amet volutpat. Gravida rutrum quisque non tellus \
          orci ac auctor. Ut sem viverra aliquet eget sit amet tellus cras adipiscing. Ultrices eros \
          in cursus turpis massa. Mollis nunc sed id semper risus in hendrerit gravida rutrum. Sed \
          blandit libero volutpat sed cras ornare arcu. Massa placerat duis ultricies lacus sed. \
          Ipsum suspendisse ultrices gravida dictum fusce ut placerat orci. Aliquet lectus proin nibh \
          nisl condimentum id venenatis a. Suspendisse potenti nullam ac tortor vitae purus faucibus \
          ornare. Sodales ut eu sem integer vitae justo eget. Maecenas volutpat blandit aliquam etiam \
          erat velit. Odio ut sem nulla pharetra diam. Duis at tellus at urna. Tempor orci dapibus \
          ultrices in iaculis nunc sed augue lacus. Hac habitasse platea dictumst quisque sagittis \
          purus sit. Arcu dictum varius duis at consectetur lorem donec. Adipiscing diam donec \
          adipiscing tristique risus nec feugiat in. Eu turpis egestas pretium aenean pharetra magna \
          ac placerat.",
          },
          {title: "POACHED",
          img: 'poached.jpg',
          contentA: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod \
          tempor incididunt ut labore et dolore magna aliqua. In egestas erat imperdiet sed euismod.\
          Maecenas sed enim ut sem viverra aliquet eget sit amet. Libero volutpat sed cras ornare \
          arcu dui vivamus arcu. Egestas sed sed risus pretium quam vulputate dignissim. Leo urna \
          molestie at elementum eu facilisis sed. In aliquam sem fringilla ut morbi tincidunt augue. \
          Egestas diam in arcu cursus euismod quis viverra. Ut eu sem integer vitae. Arcu ac tortor \
          dignissim convallis aenean. At elementum eu facilisis sed odio morbi quis commodo. \
          Fringilla ut morbi tincidunt augue interdum velit euismod. Aliquam ultrices sagittis orci \
          a scelerisque purus semper eget duis.",
          contentB: "Sit amet luctus venenatis lectus magna fringilla urna porttitor. Habitasse \
          platea dictumst quisque sagittis purus sit amet volutpat. Gravida rutrum quisque non tellus \
          orci ac auctor. Ut sem viverra aliquet eget sit amet tellus cras adipiscing. Ultrices eros \
          in cursus turpis massa. Mollis nunc sed id semper risus in hendrerit gravida rutrum. Sed \
          blandit libero volutpat sed cras ornare arcu. Massa placerat duis ultricies lacus sed. \
          Ipsum suspendisse ultrices gravida dictum fusce ut placerat orci. Aliquet lectus proin nibh \
          nisl condimentum id venenatis a. Suspendisse potenti nullam ac tortor vitae purus faucibus \
          ornare. Sodales ut eu sem integer vitae justo eget. Maecenas volutpat blandit aliquam etiam \
          erat velit. Odio ut sem nulla pharetra diam. Duis at tellus at urna. Tempor orci dapibus \
          ultrices in iaculis nunc sed augue lacus. Hac habitasse platea dictumst quisque sagittis \
          purus sit. Arcu dictum varius duis at consectetur lorem donec. Adipiscing diam donec \
          adipiscing tristique risus nec feugiat in. Eu turpis egestas pretium aenean pharetra magna \
          ac placerat.",
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
    margin: 0 2em 3em 0;
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
