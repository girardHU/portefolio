<template>
  <div id="skill-item-wrapper">
    <!-- <div class="container"> -->
      <div class="circle">
        <img :src="getImageSource()" alt="vuejs logo">
      </div>
    <!-- </div> -->
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class SkillItem extends Vue {
  @Prop() private imageName!: string;

  private getImageSource () {
    return require(`@/assets/images/${this.imageName}.png`)
  }
}
</script>

<style scoped>
.circle {
  position: relative;
  /* display: inline-block; */
  height: 7vw;
  width: 7vw;
  line-height: 60px;

  -moz-border-radius: 50%; /* or 30px */
  border-radius: 50%; /* or 30px */

  background-color: rgba(255, 255, 255, 0.300);
  /* color: white; */
  text-align: center;
  font-size: 2em;
}

.circle img {
  position: absolute;
  margin: auto;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: auto;
  /* display: block; */
  /* height: auto;
  width: 100%; */
  /* transform: translateY(5%); */
}
</style>
