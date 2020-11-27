<template>
  <div class="skills-wrapper">
    <Background imageName="toolbelt-background"/>
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
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Background from '@/components/Background.vue' // @ is an alias to /src
import ViewTitle from '@/components/ViewTitle.vue'
import SkillItem from '@/components/SkillItem.vue'

@Component({
  components: {
    Background,
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
