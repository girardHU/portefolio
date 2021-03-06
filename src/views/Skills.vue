<template>
  <div class="skills-wrapper">
    <Background imageName="toolbelt-background"/>
    <ViewTitle titleText="MY SKILL SET"/>
    <div class="skill-items-container">
      <SkillItem
        imageName="vue-logo"
        descrText="This Website is a relevant instance of what I can do!" />
      <SkillItem
        imageName="git-logo"
        descrText="I have been using Git since the very beginning of my developper's life" />
      <SkillItem
        imageName="html-logo"
        descrText="HTML is the very essence of every website, and one of the very first aspects I have dug in depth" />
      <SkillItem
        imageName="figma-logo"
        descrText="I mock up every single one of my web project with this tool" />
      <SkillItem
        imageName="javascript-logo"
        descrText="Now as essential as HTML and CSS, I use Javascript all the time, should it be with VueJS, NodeJS or other" />
      <SkillItem
        imageName="node-logo"
        descrText="My favorite Backend &quot;language&quot;, I have used it for roughly a year during my first year of work" />
      <SkillItem
        imageName="css-logo"
        descrText="The forever sidekick of HTML, I use it fluently for my every projects" />
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
