<template>
  <div>
    <Introduction/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Introduction from "@/components/homepage/Introduction.vue";
@Options({
  props: {},
  components: {
    Introduction
  }
})
export default class HomeView extends Vue {

}
</script>