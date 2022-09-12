<template>
  <div>
    <Introduction/>
    <AboutMe/>
    <Experience/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Introduction from "@/components/homepage/Introduction.vue";
import AboutMe from "@/components/homepage/AboutMe.vue";
import Experience from "@/components/homepage/Experience.vue";
@Options({
  props: {},
  components: {
    Introduction,
    AboutMe,
    Experience
  }
})
export default class HomeView extends Vue {

}
</script>