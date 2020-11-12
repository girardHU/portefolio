<template>
  <div id="about-wrapper">
    <Background imageName="moi-background"/>
    <NavigationBar current="about"/>
    <h1>This is the about page</h1>
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
export default class About extends Vue { }
</script>
