<template>
  <div>
    <nav-bar/>
      <nuxt/>
        <footer>SITE BY A. HENDRYX, 2020</footer>
  </div>
</template>



<script>
import navBar from '../components/nav-bar.vue';

export default {
  components: {
    navBar
  }
}

</script>



<style lang="scss">
@import '../assets/css/settings.variables';
@import url('https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@600&family=Barlow:wght@300&display=swap');

@mixin border-rule {
  border-top: 1px solid $ltgray;
  padding: 0 0 0.5em 0;
}

* {
  box-sizing: border-box;
}

html {
  height: 100%;
}

body {
  font-family: 'Barlow', sans-serif;
  font-family: 'Barlow Condensed', sans-serif;
  width: 85%;
  height: 100%;
  margin: 1em 0 0 2em;
}

header, h1, h2, h3 {
  font-family: 'Barlow Condensed', sans-serif;
}

h1 {
  font-family: 'Barlow', sans-serif;
  font-size: 2.7em;
  padding: 0.5em 0 0.8em 0;
}

h2 {
  font-size: 1.4em;
  padding-top: 1em;
}

h3 {
  font-size: 1em;
}

.bkgrd-img {
  height: 100%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.intro-title {
  position: absolute;
  width: 40%;
  top: 50%;
  left: 45%;
  transform: translate(-50%, -50%);
  p {
    font-size: 1.3em;
    line-height: 1.4em;
    margin-top: 0.2em;
    padding-left: 0.2em;
  }
}

p {
  font-family: 'Barlow', sans-serif;
  font-size: 0.9em;
}

footer {
  @include border-rule;
  font-size: 0.7em;
  padding: 1em 0 1em 0em;
  margin-top: 3em;
}

</style>
