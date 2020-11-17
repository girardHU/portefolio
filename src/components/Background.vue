<template>
  <div class="backround-wrapper">
    <div class="background-img" :style="getImageAsBackground()">
      <div class="layer"></div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class Background extends Vue {
  @Prop() private imageName!: string;

  private getImageAsBackground () {
    return { backgroundImage: 'url(' + require(`@/assets/images/${this.imageName}.jpg`) + ')' }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.background-img {
  position: absolute;
  top: 0;
  left: 0;
  min-width: 100%;
  min-height: 100%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;

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
