<template>
  <div class="navigation-wrapper">
    <router-link to="/home" class="nav-item home">Home</router-link>
    <router-link to="/skills" class="nav-item skills">Skills</router-link>
    <router-link to="/projects" class="nav-item projects">Projects</router-link>
    <router-link to="/work" class="nav-item work">Work</router-link>
    <router-link to="/about" class="nav-item about">About</router-link>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Watch } from 'vue-property-decorator'

@Component
export default class NavigationBar extends Vue {
  private mounted (): void {
    this.setCurrent()
  }

  @Watch('$route')
  onPropertyChange (): void {
    this.setCurrent()
  }

  private setCurrent (): void {
    let item
    console.log(this.$route.name)
    switch (this.$route.name) {
      case 'home':
        console.log('coucou home')
        item = document.querySelector('.home')
        if (item != null) {
          item.classList.add('current')
        }
        break
      case 'skills':
        console.log('coucou skills')
        item = document.querySelector('.skills')
        if (item != null) {
          item.classList.add('current')
        }
        console.log(item?.classList)
        break
      case 'projects':
        console.log('coucou projects')
        item = document.querySelector('.projects')
        if (item != null) {
          item.classList.add('current')
        }
        break
      case 'work':
        console.log('coucou work')
        item = document.querySelector('.work')
        if (item != null) {
          item.classList.add('current')
        }
        break
      case 'about':
        console.log('coucou about')
        item = document.querySelector('.about')
        if (item != null) {
          item.classList.add('current')
        }
        break
    }
  }
}
</script>

<style scoped>
.navigation-wrapper {
  display: flex;
  width: 40vw;
  margin: 3.5vh auto;
  justify-content: space-evenly;
}

@keyframes underline {
  0% {
    background-size: 0% .1em;
  }
  100%
  {
    background-size: 100% .1em;
  }
}

.nav-item {
  color: white;
  text-transform: uppercase;
  font-weight: bold;
  font-family: "Roboto Bold";
  font-size: calc(10% + 1.25vw );
  text-decoration: none;

  background: linear-gradient(#3FB984, #3FB984) bottom / 0% .1em no-repeat;
  background-position: left bottom;
  /* transition: 0.5s background-size; */
}

.current {
  text-decoration: none;
  background-size: 100% .1em;
  /* transition: 0.5s background-size; */
  /* animation: 0.5s 0s 1 underline; */
}

.nav-item:hover {
  background-size: 100% .1em;
  cursor: pointer;
}
</style>
