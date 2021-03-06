<template>
  <div class="skill-item-wrapper">
    <div class="circle">
      <img :src="getImageSource()" :alt="imageName" @click="selectSkill">
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class SkillItem extends Vue {
  @Prop() private imageName!: string;
  @Prop() private descrText!: string;

  private getImageSource () {
    return require(`@/assets/images/${this.imageName}.png`)
  }

  private selectSkill (event: any) {
    const elem = event.target.parentElement
    elem.style.animation = 'slidecenter 500ms'
    // elem.classList.add('center')
  }
}
</script>

<style scoped>
.circle {
  position: relative;
  height: 7vw;
  width: 7vw;

  -moz-border-radius: 50%;
  border-radius: 50%;

  background-color: rgba(255, 255, 255, 0.300);
  text-align: center;
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
}

.circle img:hover{
  cursor: pointer;
  animation: wiggle 95ms 2 linear;
}

@keyframes wiggle {
    0% { transform: rotate(0deg); }
   30% { transform: rotate(0deg); }
   35% { transform: rotate(4deg); }
   65% { transform: rotate(-5deg); }
  100% { transform: rotate(0deg); }
}

@keyframes slidecenter {
  /* from {
    margin-left: 100%;
    width: 300%;
  } */

  to {
    position: absolute;
    left: 50%;
    top: 50%;
    margin-left: -7vw;
    margin-top: -7vh;
  }
}
</style>
