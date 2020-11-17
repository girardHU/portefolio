<template>
  <div class="view-title-wrapper">
    <h1>{{titleText}}</h1>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class ViewTitle extends Vue {
  @Prop() private titleText!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-family: "Roboto Slab";
  color: white;
  text-align: center;
  margin: 8vh 0 4vh 0;
  font-size: 2vw;
}
</style>
