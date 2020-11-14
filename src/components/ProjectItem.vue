<template>
  <div id="project-item-wrapper">
    <div class="project">
      <img :src="getImageSource()" :alt="image" class="screenshot">
      <h5>{{ name }}</h5>
      <h6>{{ startDate }} - {{ endDate }}</h6>
      <h6>INVESTIGATE ON THIS PROJECT</h6>
      <div class="link-container">
        <img src="@/assets/images/link-icon.png" alt="link-icon" class="link-icon">
        <img src="@/assets/images/github-icon.png" alt="github-icon" class="github-icon">
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
  @Prop({ default: 'none' }) private projectLink!: string;
  @Prop({ default: 'none' }) private githubLink!: string;

  private getImageSource () {
    return require(`@/assets/images/${this.image}.jpg`)
  }
}
</script>
