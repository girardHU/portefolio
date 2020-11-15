<template>
  <div id="projects-wrapper">
    <Background imageName="working-background"/>
    <NavigationBar/>
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
    <NavigationButtons/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Background from '@/components/Background.vue' // @ is an alias to /src
import NavigationBar from '@/components/NavigationBar.vue'
import NavigationButtons from '@/components/NavigationButtons.vue'
import ViewTitle from '@/components/ViewTitle.vue'
import ProjectItem from '@/components/ProjectItem.vue'

@Component({
  components: {
    Background,
    NavigationBar,
    NavigationButtons,
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
  margin-bottom: 2%;
}
</style>
