<template>
  <div id="projects-wrapper">
    <Background imageName="working-background"/>
    <NavigationBar current="projects"/>
    <h1>This is the projects page</h1>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Background from '@/components/Background.vue' // @ is an alias to /src
import NavigationBar from '@/components/NavigationBar.vue'

@Component({
  components: {
    Background,
    NavigationBar
  }
})
export default class Projects extends Vue { }
</script>
