<template>
  <div id="nav">
    <nuxt-link to="/">HOME</nuxt-link>
    <nuxt-link to="/how-to">HOW TO</nuxt-link>
    <nuxt-link to="/know-your-egg">KNOW YOUR EGG</nuxt-link>
    <nuxt-link to="/recipes">RECIPES</nuxt-link>
  </div>
</template>


<style lang="scss">
@import '../assets/css/settings.variables';

#nav {
  padding: 2em 1em 2em 0;
}

#nav a {
  font-size: 1em;
  padding: 0.1em 0.7em 0.21em 0.7em;
  margin-right: 0.7em;
  text-align: center;
  cursor: pointer;
  text-decoration: none;
  color: #4d4d4d;
}

#nav a.nuxt-link-exact-hover {
  color: #4d4d4d;
}

#nav a.nuxt-link-exact-active {
  color: #4d4d4d;
}

a {
    text-decoration: none;
    border: 1px solid $yellow;
    line-height: 0.7em;
    background-color: #fff;
}

a:hover {
  color: $dkgray;
  box-shadow: inset 0 -3em 0 0 $yellow;
  transition: 0.25s;
}


/* Adding media query for nav bar */
@media screen and (max-width: 480px) {

  #nav {
    display: flex;
    flex-flow: column;
    width: 45%;
  }

  #nav a {
    font-size: 1em;
    padding: 0.5em 0em 0.5em 0.8em;
    margin-bottom: 0.2em;
    text-align: left;
    cursor: pointer;
    text-decoration: none;
    color: #4d4d4d;
  }
}


</style>
