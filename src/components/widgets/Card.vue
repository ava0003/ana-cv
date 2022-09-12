<template>
    <div class="card-wrapper">
        <div
            :style="`background-image:${iconPathValue}`"
            class="icon">
        </div>
        <div class="title">
          <div>{{ title }}</div>
        </div>
        <div class="description">
          <div>{{ description }}</div>
        </div>
    </div>
</template>

<script lang="ts">
import { Options, Vue, } from 'vue-class-component';

@Options({
  props: {
    iconPath: String,
    title: String,
    description : String

  },
  components: {
  }
})
export default class Card extends Vue {
    iconPath!: string;
    title!: string;
    description!: string


    get iconPathValue() {
        return this.iconPath;
    }
}
</script>

<style lang="less" scoped>

  @spacer: 50px;
  @2spacer: @spacer * 2;
  @4spacer: @spacer * 4;

    .card-wrapper {
        position: relative;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-align: center;
        padding: 5px;
        background-color: white;
        color: black;
        display: flex;
        border: 1px solid black;
        height: 100% ;

        .title{
          margin-bottom: 2px;
          font-weight: bold;
          font-size: 1.2em;
        }
        .icon{
          position: relative;
          height: 30%;
          width: 30%;
          // top: calc(50% - 37%);
          // left: calc(50% - 32%);
          background-image: url("@/assets/img/descarga.png");
          background-size: cover;
          background-position: center;
          background-repeat: no-repeat;
        }
    }
</style>
