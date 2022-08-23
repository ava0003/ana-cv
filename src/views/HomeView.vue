<template>
  <div>
    <Introduction/>
    <AboutMe/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Introduction from "@/components/homepage/Introduction.vue";
import AboutMe from "@/components/homepage/AboutMe.vue";
@Options({
  props: {},
  components: {
    Introduction,
    AboutMe
  }
})
export default class HomeView extends Vue {

}
</script>