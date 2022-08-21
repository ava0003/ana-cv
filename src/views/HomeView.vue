<template>
  <div>
    <Section1/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Section1 from "@/components/homepage/Section1.vue";
@Options({
  props: {},
  components: {
    Section1
  }
})
export default class HomeView extends Vue {

}
</script>