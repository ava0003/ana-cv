<template>
  <!-- <MyHeader></MyHeader> -->
  <router-view/>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import MyHeader from '@/components/header/MyHeader.vue'
@Options({
  props: {},
  components: {
    MyHeader
  }
})
export default class App extends Vue {

}
</script>

<style>
html, body {
  padding: 0;
  margin : 0;
}
* {
  box-sizing: border-box;
}
</style>
