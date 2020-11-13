<template>
  <div id="skills-wrapper">
    <Background imageName="toolbelt-background"/>
    <NavigationBar/>
    <ViewTitle titleText="MY SKILL SET"/>
    <NavigationButtons/>

  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Background from '@/components/Background.vue' // @ is an alias to /src
import NavigationBar from '@/components/NavigationBar.vue'
import NavigationButtons from '@/components/NavigationButtons.vue'
import ViewTitle from '@/components/ViewTitle.vue'

@Component({
  components: {
    Background,
    NavigationBar,
    NavigationButtons,
    ViewTitle
  }
})
export default class Skills extends Vue { }
</script>
