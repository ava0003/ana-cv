<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h3>{{ msg2 }}</h3>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    msg: String,
    msg2: {
      type: String, 
      default : "TOTO2",
      required : true 
    }
  }
})
export default class HelloWorld extends Vue {
  msg!: string
  msg2!: string
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
