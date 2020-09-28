<template>
  <div id="work-wrapper">
    <Background imageName="road-background"/>
    <NavigationBar current="work"/>
    <h1>This is the work page</h1>
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
export default class Work extends Vue { }
</script>
