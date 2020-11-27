<template>
  <div id="app">
    <NavigationBar/>
    <!-- <NavigationButtons/> -->
    <router-view/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import NavigationBar from '@/components/NavigationBar.vue'
import NavigationButtons from '@/components/NavigationButtons.vue'

@Component({
  components: {
    NavigationBar,
    NavigationButtons
  }
})

export default class App extends Vue { }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

h1, h2, h3, h4, h5, h6, p {
  cursor: default;
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

@font-face {
  font-family: "Roboto Slab Thin";
  src: local("Roboto Slab Thin"),
    url(./assets/fonts/robotoSlab/RobotoSlab-Thin.ttf) format("truetype");
}

@font-face {
  font-family: "Roboto Slab Light";
  src: local("Roboto Slab Light"),
    url(./assets/fonts/robotoSlab/RobotoSlab-Light.ttf) format("truetype");
}
</style>
