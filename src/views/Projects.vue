<template>
  <div id="projects-wrapper">
    <Background imageName="working-background"/>
    <NavigationBar/>
    <h1>This is the projects page</h1>
    <NavigationButtons/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Background from '@/components/Background.vue' // @ is an alias to /src
import NavigationBar from '@/components/NavigationBar.vue'
import NavigationButtons from '@/components/NavigationButtons.vue'

@Component({
  components: {
    Background,
    NavigationBar,
    NavigationButtons
  }
})
export default class Projects extends Vue { }
</script>
