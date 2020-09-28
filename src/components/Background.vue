<template>
  <div class="backround-wrapper">
    <img class="background-img" :src="getImage()" alt="background image">
    <div class="layer">
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class Background extends Vue {
  @Prop() private imageName!: string;

  private getImage () {
    return require(`../assets/images/${this.imageName}.jpg`)
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

  object-fit: cover;
  pointer-events: none;
  z-index: -1;
}
.layer {
  background-color: rgba(0, 0, 0, 0.5);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
  z-index: -1;
}
</style>
