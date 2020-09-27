<template>
  <div class="backround">
    <img class="background-img" :src="imagePath()">
    <div class="layer">
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class Background extends Vue {
  @Prop() private image!: string;

  private imagePath () {
    return require(`../assets/images/${this.image}.jpg)`)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.background-img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  /* background-image: url("../assets/images/code-background.jpg"); */
  background-position: center/fixed;
  background-repeat: no-repeat;
  background-size: cover;
}
.layer {
  background-color: rgba(0, 0, 0, 0.5);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
