<template>
  <div id="skills-wrapper">
    <Background imageName="toolbelt-background"/>
    <NavigationBar current="skills"/>
    <h1>This is the Skills page</h1>
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
export default class Skills extends Vue { }
</script>
