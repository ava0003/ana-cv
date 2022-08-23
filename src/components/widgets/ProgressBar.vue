<template>
    <div class="progress-container">
        <p class="progress-label">{{ item }}</p>
        <div class="progress-bar">
            <progress></progress>
        </div>
    </div>
</template>

<script lang="ts">
import { Options, Vue, } from 'vue-class-component';

@Options({
  props: {
    item : String,
    percentage : Number

  },
  components: {
  }
})
export default class ProgressBar extends Vue {
    item!: string
    percentage!: number
}
</script>

<style lang="less" scoped>
    progress {
        opacity: 0;
    }
    .progress-container {
        position: relative;
        widows: 100%;
        .progress-label {
            position: relative;
        }

        .progress-label::after {
            content: "75 %";
            position: absolute;
            top:0;
            right: 0;
        }

        .progress-bar {
        position: relative;
        display: inline-block;
        background: #eee;
        border-radius: 6px;
        overflow: hidden;
        width: 100%;
        }

        .progress-bar::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 75%;
        background: rgb(0, 2, 2);
        }


    }


</style>
