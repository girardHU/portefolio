<template>
  <div class="navigation-wrapper">
    <router-link to="/home" class="nav-item home">Home</router-link>
    <router-link to="/skills" class="nav-item skills">Skills</router-link>
    <router-link to="/projects" class="nav-item projects">Projects</router-link>
    <router-link to="/work" class="nav-item work">Work</router-link>
    <router-link to="/about" class="nav-item about">About</router-link>

    <NavigationButtons/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import NavigationButtons from '@/components/NavigationButtons.vue'

@Component({
  components: {
    NavigationButtons
  }
})
export default class NavigationBar extends Vue { }
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
  transition: 0.3s background-size;
}

.router-link-active {
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
