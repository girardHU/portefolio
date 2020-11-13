<template>
  <div id="skills-wrapper">
    <Background imageName="toolbelt-background"/>
    <NavigationBar/>
    <h1>This is the Skills page</h1>
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
export default class Skills extends Vue { }
</script>
