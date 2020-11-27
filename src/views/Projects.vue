<template>
  <div class="projects-wrapper">
    <Background imageName="working-background"/>
    <ViewTitle titleText="MY PROJECTS"/>
    <div class="projects-container">
      <ProjectItem class="prj-item" name="Portefolio" image="test-img" startDate="Aug 2020" endDate="Nov 2020" githubLink="https://github.com/girardHU/portefolio/tree/dev"/>
      <ProjectItem class="prj-item" name="Portefolio" image="test-img" startDate="Aug 2020" endDate="Nov 2020"/>
      <ProjectItem class="prj-item" name="Portefolio" image="test-img" startDate="Aug 2020" endDate="Nov 2020"/>
      <ProjectItem class="prj-item" name="Portefolio" image="test-img" startDate="Aug 2020" endDate="Nov 2020"/>
      <ProjectItem class="prj-item" name="Portefolio" image="test-img" startDate="Aug 2020" endDate="Nov 2020"/>
      <ProjectItem class="prj-item" name="Portefolio" image="test-img" startDate="Aug 2020" endDate="Nov 2020"/>
      <ProjectItem class="prj-item" name="Portefolio" image="test-img" startDate="Aug 2020" endDate="Nov 2020"/>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Background from '@/components/Background.vue' // @ is an alias to /src
import ViewTitle from '@/components/ViewTitle.vue'
import ProjectItem from '@/components/ProjectItem.vue'

@Component({
  components: {
    Background,
    ViewTitle,
    ProjectItem
  }
})
export default class Projects extends Vue { }
</script>

<style scoped>
.projects-container {
  width: 72%;
  display: flex;
  margin: auto;
  flex-wrap: wrap;
  justify-content: space-around;
}
.prj-item {
  flex: 1 0 21%;
  margin-bottom: 2%;
}
</style>
