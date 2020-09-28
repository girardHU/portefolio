<template>
  <div class="home">
    <Background imageName="code-background"/>
      <div id="wrapper">
        <vue-typed-js :strings="['a FullStack Developer', 'a Tech Enthusiast', 'an Everyday Learner']"
        loop="true"
        smartBackspace="true"
        backDelay="1500">
          <h1 id="hello-text" class="home-text">
            Hello! My name is Hugo Girard and I am<br><span class="typing"></span>
          </h1>
        </vue-typed-js>
      </div>
      <h3 id="footer-text" class="home-text">
        this website is showcased in english, yet i am french
      </h3>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Background from '@/components/Background.vue' // @ is an alias to /src

@Component({
  components: {
    Background
  }
})
export default class Home extends Vue { }
</script>

<style>
.home-text {
  text-transform: uppercase;
  position: fixed;
}

#hello-text {
  text-align: left;
  font-family: "Roboto Condensed Regular";
  font-size: 48px;
  top: 45vh;
  left: 10vh;
  color: white;
}

#footer-text {
  font-family: "Roboto Condensed Light";
  font-size: 24px;
  bottom: 2vh;
  right: 4vh;
  color: rgba(255, 255, 255, 0.3);
}

/* #wrapper {
  background-color: teal;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

#cursor {
  display: inline-block;
  width: 3px;
  height: 40px;
  background-color: #ccc;
  margin-left: 0.1rem;
  animation: blink 1s infinite;
}
.cursor.typing {
  animation: none;
}
@keyframes blink {
  0% {background-color: #ccc;}
  49% {background-color: #ccc;}
  50% {background-color: transparent;}
  99% {background-color: transparent;}
  100% {background-color: #ccc;}
} */

</style>
