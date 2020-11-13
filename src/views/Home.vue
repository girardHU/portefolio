<template>
  <div id="home-wrapper">
    <Background imageName="code-background"/>
    <NavigationBar/>
    <vue-typed-js :strings="['a FullStack Developer', 'a Tech Enthusiast', 'an Everyday Learner', 'passionate']"
    loop="true"
    smartBackspace="true"
    backDelay="1500">
    <h1 id="hello-text" class="home-text">
      Hello! My name is Hugo Girard and I am<br><span class="typing"></span>
    </h1>
    </vue-typed-js>
    <NavigationButtons/>
    <h3 id="footer-text" class="home-text">
      this website is showcased in english, yet i am french
    </h3>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Background from '@/components/Background.vue' // @ is an alias to /src
import NavigationBar from '@/components/NavigationBar.vue'
import NavigationButtons from '@/components/NavigationButtons.vue'

@Component({
  components: {
    Background,
    NavigationBar,
    NavigationButtons
  }
})

export default class Home extends Vue { }
</script>

<style>
.home-text {
  text-transform: uppercase;
  position: fixed;
  cursor: default;
}

#hello-text {
  text-align: left;
  font-family: "Roboto Condensed Regular";
  font-size: 3vw;
  top: 42vh;
  left: 10vh;
  color: white;
}

#footer-text {
  font-family: "Roboto Condensed Light";
  font-size: 1vw;
  bottom: 2vh;
  right: 4vh;
  color: rgba(255, 255, 255, 0.3);
}

</style>
