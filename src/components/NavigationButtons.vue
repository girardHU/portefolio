<template>
  <div id="navigation-button-wrapper">
    <img id="back-button" class="navigation-button" :src="sourceBack"/>
    <img id="next-button" class="navigation-button" :src="sourceNext"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class NavigationButtons extends Vue {
  private isBack = false;
  private isNext = false;
  private sourceBack = require('@/assets/images/back_button.png')
  private sourceNext = require('@/assets/images/next_button.png')

  private created (): void {
    this.setCurrent()
  }

  private setCurrent (): void {
    this.isBack = false
    this.isNext = false
  }
}
</script>

<style>
.navigation-button {
  position: absolute;
  z-index: 0;
}

#back-button {
  top: 48vh;
  left: 3vw;
}

#next-button {
  top: 48vh;
  right: 3vw;
}
</style>
