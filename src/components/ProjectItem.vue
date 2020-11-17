<template>
  <div class="project-item-wrapper">
    <div class="project-item">
      <img :src="getImageSource()" :alt="image" class="screenshot project-child">
      <h5 class="title project-child">{{ name }}</h5>
      <h6 class="project-child">{{ startDate }} - {{ endDate }}</h6>
      <h6 class="project-child">INVESTIGATE ON THIS PROJECT</h6>
      <div class="link-container project-child">
        <img src="@/assets/images/link-icon.png" :class="{clickable: projectLink}" @click="redirectProject" alt="link-icon" class="link-icon icon">
        <img src="@/assets/images/github-icon.png" :class="{clickable: githubLink}" @click="redirectGithub" alt="github-icon" class="github-icon icon">
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class ProjectItem extends Vue {
  @Prop() private name!: string;
  @Prop() private image!: string;
  @Prop() private startDate!: string;
  @Prop({ default: 'running' }) private endDate!: string;
  @Prop({ default: false }) private projectLink!: string;
  @Prop({ default: false }) private githubLink!: string;

  private getImageSource () {
    return require(`@/assets/images/${this.image}.jpg`)
  }

  private redirectProject () {
    if (this.projectLink) {
      window.open(this.projectLink)
    }
  }

  private redirectGithub () {
    if (this.githubLink) {
      window.open(this.githubLink)
    }
  }
}
</script>

<style scoped>
.project-item {
  /* height: 17.3vw;
  width: 12vw; */
  height: calc(130px + 10vw);
  width: calc(95px + 8vw);
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  background-color: #232f5977;
  margin: auto;
  border-radius: 2%;
}

.project-child {
  margin: 0 auto;
  font-size: calc(30% + 0.5vw);
  color: white;
}

.project-item .title {
  font-size: 0.85vw;
}

.clickable {
  cursor: pointer;
  transition: transform .2s;
}

.screenshot {
  width: 95%;
  height: auto;
  border-radius: 3%;
  margin-top: -5%;
}

.link-container {
  display: flex;
  justify-content: space-around;
}

.icon {
  width: 10%;
  height: auto;
}

.clickable:hover {
transform: scale(1.3);
}
</style>
