<template>
  <div id="navigation-wrapper">
    <div id="home" class="nav-item">Home</div>
    <div id="skills" class="nav-item">Skills</div>
    <div id="projects" class="nav-item">Projects</div>
    <div id="work" class="nav-item">Work</div>
    <div id="about" class="nav-item">About</div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class NavigationBar extends Vue {
  @Prop() private current!: string;
}
</script>

<style>
#navigation-wrapper {
  display: flex;
  width: 40vw;
  margin: 3.5vh auto;
  justify-content: space-evenly;
}

.nav-item {
  background: linear-gradient(#3FB984, #3FB984) bottom / 0% .1em no-repeat;
  background-position: left bottom;
  transition: 0.5s background-size;
}

.nav-item:hover {
  background-size: 100% .1em;
  cursor: pointer;
}

.nav-item {
  color: white;
  text-transform: uppercase;
  font-weight: bold;
  font-family: "Roboto Bold";
  font-size: 24px;
}
</style>
