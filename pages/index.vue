<template>
  <div>
    <img class="bkgrd-img" src="../assets/egg-bkgrd.jpg" width=95% alt="Close-up of eggs scattered on a surface">
     <section class="intro-title">
        <img src="../assets/type-treatmt-gray.svg" width=80%>
          <p>Eggs are a great, inexpensive source of protein, and one of the few foods
            that naturally offer vitamin D. They're also incredibly versatile. So, why only eat them for breakfast?
            Check out some ideas for making eggs part of your meal any time of day.</p>
     </section>
  </div>
</template>


<style lang="scss">

.bkgrd-img {
  position: fixed;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
}

.intro-title {
  position: absolute;
  width: 40%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  p {
    font-size: 1.3em;
    line-height: 1.4em;
    margin-top: 0.2em;
    padding-left: 0.2em;
  }
}


/* Adding a media query for mobile */
@media screen and (max-width: 480px) {

  .bkgrd-img {
    width: 175%;
    left: 0;
  }

  .intro-title {
    width: 80%;
    top: 65%;
  }

}

</style>
