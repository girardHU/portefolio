<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

@font-face {
  font-family: "Roboto Condensed Regular";
  src: local("Roboto Condensed Regular"),
    url(./assets/fonts/robotoCondensed/RobotoCondensed-Regular.ttf) format("truetype");
}

@font-face {
  font-family: "Roboto Condensed Light";
  src: local("Roboto Condensed Light"),
    url(./assets/fonts/robotoCondensed/RobotoCondensed-Light.ttf) format("truetype");
}

@font-face {
  font-family: "Roboto Bold";
  src: local("Roboto Bold"),
    url(./assets/fonts/roboto/Roboto-Bold.ttf) format("truetype");
}

</style>
