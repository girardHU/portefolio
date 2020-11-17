<template>
  <div class="work-wrapper">
    <Background imageName="road-background"/>
    <NavigationBar/>
    <ViewTitle titleText="MY EXPERIENCE"/>
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
export default class Work extends Vue { }
</script>
