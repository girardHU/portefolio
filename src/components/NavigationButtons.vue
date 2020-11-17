<template>
  <div class="navigation-button-wrapper">
    <div class="navigation-button-container prev-btn" v-if="isBack">
      <div class="navigation-button-center">
        <button class="navigation-button-btn" v-on:click="handlePrev">
          <svg viewBox="0 0 180 60" class="border">
            <polyline points="179,1 179,59 1,59 1,1 179,1" class="bg-line" />
            <polyline points="179,1 179,59 1,59 1,1 179,1" class="hl-line" />
          </svg>
          <span>PREVIOUS</span>
        </button>
      </div>
    </div>
    <div class="navigation-button-container next-btn"  v-if="isNext">
      <div class="navigation-button-center">
        <button class="navigation-button-btn" v-on:click="handleNext">
          <svg viewBox="0 0 180 60" class="border">
            <polyline points="179,1 179,59 1,59 1,1 179,1" class="bg-line" />
            <polyline points="179,1 179,59 1,59 1,1 179,1" class="hl-line" />
          </svg>
          <span>NEXT</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class NavigationButtons extends Vue {
  private isBack = true;
  private isNext = true;
  private routes = ['home', 'skills', 'projects', 'work', 'about']

  private mounted (): void {
    this.setVisibility()
  }

  private setVisibility (): void {
    if (this.$route.name === this.routes[0]) this.isBack = false
    if (this.$route.name === this.routes[this.routes.length - 1]) this.isNext = false
  }

  private handlePrev (): void {
    const currentIndex = this.routes.findIndex(element => element === this.$route.name)
    this.$router.push(this.routes[currentIndex - 1])
  }

  private handleNext (): void {
    const currentIndex = this.routes.findIndex(element => element === this.$route.name)
    this.$router.push(this.routes[currentIndex + 1])
  }
}
</script>

<style scoped>
.navigation-button {
  position: absolute;
  z-index: -1;
}

.navigation-button-container.prev-btn {
  left: 6.5vw;
  top: 49vh;
}

.navigation-button-container.next-btn {
  right: 1.5vw;
  top: 49vh;
}

.navigation-button-container {
  width: 100px;
  height: 100px;
  position: absolute;
  transform: translate(-50%, -50%);
  display: flex;
  justify-content: center;
  align-items: center;
}

.navigation-button-center {
  width: 180px;
  height: 60px;
  position: absolute;
}

.navigation-button-btn {
  width: 9vw;
  height: 6vh;
  cursor: pointer;
  background: transparent;
  border: 1px solid #3fb9847a;
  outline: none;
  /* border-radius: 4cm; */
  transition: 1s ease-in-out;
}

svg {
  position: absolute;
  left: 0;
  top: 0;
  height: 6vh;
  width: 9vw;
  fill: none;
  stroke: #fff;
  stroke-dasharray: 150 480;
  stroke-dashoffset: 150;
  transition: 1s ease-in-out;
}

.navigation-button-btn:hover {
  transition: 1s ease-in-out;
  background: #3fb9842f;
}

.navigation-button-btn:hover svg {
  stroke-dashoffset: -480;
}

.navigation-button-btn span {
  color: white;
  font-size: 18px;
  font-weight: 100;
}

</style>
