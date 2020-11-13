<template>
  <div id="work-wrapper">
    <Background imageName="road-background"/>
    <NavigationBar/>
    <h1>This is the work page</h1>
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
export default class Work extends Vue { }
</script>
