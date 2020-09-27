<template>
  <div class="home">
    <Background image="code-background"/>
      <h1 class="hello-text">
        Hello! My name is Hugo Girard and I am a<br>fullstack developer
      </h1>
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
export default class Home extends Vue {}
</script>

<style>

.hello-text {
  /* background-color: violet; */
  text-align: left;
  font-family: "Roboto Condensed Light";
  /* font-size: 48; */
  text-transform: uppercase;
  position: fixed;
  top: 45%;
  left: 10%;
  color: white;
}
</style>
