<template>
  <div class="work-wrapper">
    <Background imageName="road-background"/>
    <ViewTitle titleText="MY EXPERIENCE"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Background from '@/components/Background.vue' // @ is an alias to /src
import ViewTitle from '@/components/ViewTitle.vue'

@Component({
  components: {
    Background,
    ViewTitle
  }
})
export default class Work extends Vue { }
</script>
