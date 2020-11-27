<template>
  <div class="about-wrapper">
    <Background imageName="moi-background"/>
    <ViewTitle titleText="ABOUT ME"/>
    <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae consequatur, vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?</p>
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
export default class About extends Vue { }
</script>

<style scoped>
p {
  font-family: "Roboto Slab Light";
  font-size: 1.3vw;
  color: white;
  width: 30vw;
  text-align: justify;
  margin-left: auto;
  margin-right: auto;
}
</style>
