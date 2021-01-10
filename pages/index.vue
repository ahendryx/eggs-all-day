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
@import '../assets/css/settings.variables';

.bkgrd-img {
  position: fixed;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
}

.intro-title {
  position: absolute;
  width: 45%;
  top: 55%;
  left: 55%;
  transform: translate(-50%, -50%);
  p {
    font-size: 1.3em;
    line-height: 1.4em;
    margin-top: 0.2em;
    padding-left: 0.2em;
  }
  img {
    padding-bottom: 0.8em;
  }
}


/* Adding a media query for mobile */
@media screen and (min-width: 300px) and (max-width: 480px) {

.bkgrd-img {
  width: 800px;
  left: 0;
  overflow: hidden;
  opacity: 65%;
}

.intro-title {
  width: 85%;
  top: 60%;
}

footer {
  opacity: 0%;
}

}

@media screen and (min-width: 600px) and (max-width: 800px) {

.bkgrd-img {
  width: 800px;
  left: 0;
  overflow: hidden;
}

.intro-title {
  top: 40%;
}

}


</style>
