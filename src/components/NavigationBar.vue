<template>
  <div id="navigation-wrapper">
    <router-link to="/home" id="home" class="nav-item">Home</router-link>
    <router-link to="/skills" id="skills" class="nav-item">Skills</router-link>
    <router-link to="/projects" id="projects" class="nav-item">Projects</router-link>
    <router-link to="/work" id="work" class="nav-item">Work</router-link>
    <router-link to="/about" id="about" class="nav-item">About</router-link>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class NavigationBar extends Vue {
  @Prop() private current!: string;

  private mounted (): void {
    this.setCurrent()
  }

  private setCurrent (): void {
    let item
    switch (this.current) {
      case 'home':
        item = document.querySelector('#home')
        if (item != null) {
          item.classList.add('current')
        }
        break
      case 'skills':
        item = document.querySelector('#skills')
        if (item != null) {
          item.classList.add('current')
        }
        break
      case 'projects':
        item = document.querySelector('#projects')
        if (item != null) {
          item.classList.add('current')
        }
        break
      case 'work':
        item = document.querySelector('#work')
        if (item != null) {
          item.classList.add('current')
        }
        break
      case 'about':
        item = document.querySelector('#about')
        if (item != null) {
          item.classList.add('current')
        }
        break
    }
  }
}
</script>

<style>
#navigation-wrapper {
  display: flex;
  width: 40vw;
  margin: 3.5vh auto;
  justify-content: space-evenly;
}

.nav-item.current {
  text-decoration: none;
  background-size: 100% .1em;
  transition: none;
}

.nav-item {
  color: white;
  text-transform: uppercase;
  font-weight: bold;
  font-family: "Roboto Bold";
  font-size: 24px;
  text-decoration: none;

  background: linear-gradient(#3FB984, #3FB984) bottom / 0% .1em no-repeat;
  background-position: left bottom;
  transition: 0.5s background-size;
}

.nav-item:hover {
  background-size: 100% .1em;
  cursor: pointer;
}
</style>
