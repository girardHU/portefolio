<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
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

@font-face {
  font-family: "Roboto Slab";
  src: local("Roboto Slab"),
    url(./assets/fonts/robotoSlab/RobotoSlab-Regular.ttf) format("truetype");
}
</style>
