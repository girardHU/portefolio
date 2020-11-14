<template>
  <div id="skill-item-wrapper">
    <div class="container">
      <div class="circle">
        <img :src="getImageSource()" alt="vuejs logo">
      </div>
    </div>
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  width: 6vw;
  height:auto;
  /* background: blue; */
}

.circle {
  border-radius: 50%;
  width: 100%;
  padding-bottom: auto;
  background: rgba(255, 255, 255, 0.287);
}

.circle img {
  height: auto;
  width: 100%;
  transform: translateY(5%);
}
</style>
