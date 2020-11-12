<template>
  <div id="navigation-button-wrapper">
    <img id="back-button" class="navigation-button" v-if="isBack" :src="sourceBack"/>
    <img id="next-button" class="navigation-button" v-if="isNext" :src="sourceNext"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class NavigationButtons extends Vue {
  private isBack = true;
  private isNext = true;
  private sourceBack = require('@/assets/images/back_button.png')
  private sourceNext = require('@/assets/images/next_button.png')

  private mounted (): void {
    this.setVisibility()
  }

  private setVisibility (): void {
    if (this.$route.name === 'Home') this.isBack = false
    if (this.$route.name === 'About') this.isNext = false
  }
}
</script>

<style>
.navigation-button {
  position: absolute;
  z-index: -1;
}

#back-button {
  top: 48vh;
  left: 1.5vw;
}

#next-button {
  top: 48vh;
  right: 1.5vw;
  max-width: 100%;
  height: auto;
}
</style>
