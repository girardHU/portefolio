<template>
  <div id="skills-wrapper">
    <Background imageName="toolbelt-background"/>
    <NavigationBar/>
    <ViewTitle titleText="MY SKILL SET"/>
    <div class="skill-items-container">
      <SkillItem imageName="vue-logo"/>
      <SkillItem imageName="git-logo"/>
      <SkillItem imageName="html-logo"/>
      <SkillItem imageName="figma-logo"/>
      <SkillItem imageName="javascript-logo"/>
      <SkillItem imageName="node-logo"/>
      <SkillItem imageName="css-logo"/>
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
import SkillItem from '@/components/SkillItem.vue'

@Component({
  components: {
    Background,
    NavigationBar,
    NavigationButtons,
    ViewTitle,
    SkillItem
  }
})
export default class Skills extends Vue { }
</script>

<style scoped>
.skill-items-container {
  margin: 10vh auto auto auto;
  width: 34vw;
  height: 20vw;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}

</style>
