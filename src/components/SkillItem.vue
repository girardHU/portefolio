<template>
  <div class="skill-item-wrapper">
      <div class="item-hints">
        <div class="circle hint" data-position="4">
          <img :src="getImageSource()" :alt="imageName">
          <span class="hint-radius"></span>
          <div class="hint-content do--split-children">
            <!-- <p>The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English.</p> -->
            <p>{{ tooltipText }}</p>
          </div>
        </div>
      </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import '@/components/vapor-tooltip.css'

@Component
export default class SkillItem extends Vue {
  @Prop() private imageName!: string;
  @Prop() private tooltipText!: string;

  private getImageSource () {
    return require(`@/assets/images/${this.imageName}.png`)
  }
}
</script>

<style scoped>
.circle {
  position: relative;
  height: 7vw;
  width: 7vw;

  -moz-border-radius: 50%;
  border-radius: 50%;

  background-color: rgba(255, 255, 255, 0.300);
  text-align: center;
}

.circle img {
  position: absolute;
  margin: auto;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: auto;
}
</style>
