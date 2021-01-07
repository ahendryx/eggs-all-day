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

body {
  font-family: 'Barlow', sans-serif;
  font-family: 'Barlow Condensed', sans-serif;
  width: 90%;
  height: 100%;
  margin: 1em 0 0 2em;
}

header, h1, h2, h3, h4 {
  font-family: 'Barlow Condensed', sans-serif;
}

h1 {
  font-family: 'Barlow', sans-serif;
  font-size: 2.7em;
  padding-top: 0.5em;
}

h2 {
  font-size: 1.4em;
  padding-top: 1em;
}

h3 {
  font-size: 1.2em;
  padding-top: 2em;
}

h4 {
  font-size: 0.9em;
  font-weight: 600;
  border-top: 1px dotted $dkgray;
  padding-top: 0.5em;
  margin-top: 3.5em;
}

p {
  font-family: 'Barlow', sans-serif;
  font-size: 0.9em;
  line-height: 1.5em;
}

footer {
  @include border-rule;
  font-size: 0.7em;
  padding: 1em 0 1em 0em;
  margin-top: 3em;
}


</style>
