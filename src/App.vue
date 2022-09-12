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

@font-face {
 font-family: "Montserrat";
 src: url("@/assets/fonts/montserrat/Montserrat.ttf") format("truetype");
}


html, body {
  padding: 0;
  margin : 0;
  font-family: Montserrat !important;
}
* {
  box-sizing: border-box;
}
</style>
