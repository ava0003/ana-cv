<template>
    <div class="section1">Section 1
        <div class="child">Child</div>

    </div>
    <div class="row g-4 py-5 row-cols-1 row-cols-lg-6">
        <div class="col-lg-6">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro ut molestiae harum, quia, adipisci explicabo soluta ipsa amet commodi dolorem optio voluptatibus eaque, debitis sed ullam. Asperiores perferendis nostrum animi!
        </div>
        <div class="col-lg-6">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro ut molestiae harum, quia, adipisci explicabo soluta ipsa amet commodi dolorem optio voluptatibus eaque, debitis sed ullam. Asperiores perferendis nostrum animi!
        </div>
    </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import "bootstrap/dist/css/bootstrap.min.css";
import "bootstrap";

@Options({
  props: {},
  components: {
  }
})
export default class Section1 extends Vue {

}
</script>

<style lang="less" scoped>

.section1 {
  padding: 0;
  margin : 0;
  background-color: green;
  color: yellow;
//  .child{ Only apply to child
//    background-color: purple;
//}
}
.child{
    color: yellow;
}
</style>
