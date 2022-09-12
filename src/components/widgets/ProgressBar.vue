<template>
    <div class="progress-container">
        <div class="progress-label">
            <div>{{ item }}</div>
        </div>
        <div class="progress-bar-container">

            <div
            :style="`width:${percentageValue}%`"
            class="progress">

            </div>

        </div>
    </div>
</template>

<script lang="ts">
import { Options, Vue, } from 'vue-class-component';

@Options({
  props: {
    item: String,
    percentage: {
        type: Number,
        default: 0,
        required: true
    }

  },
  components: {
  }
})
export default class ProgressBar extends Vue {
    // eslint-disable-next-line
    [x: string]: any;
    item!: string;
    animated = false;

    mounted() {
        this.animated = true;
    }

    get percentageValue() {
        return this.percentage;
    }

}
</script>

<style lang="less" scoped>

    .align-r {
        display: flex;
        align-self: flex-end;
    }

    @keyframes animated{
        0%   {margin-left: -100%;}
        100% {margin-left: 0%;}
    }
    .progress-container {
        position: relative;
        display: flex;
        flex-direction: column;
        margin-bottom: 15px;
        width: 100%;
        .progress-label {
            position: relative;
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            margin-bottom: 5px;
        }

        .progress-bar-container {
            position: relative;
            display: flex;
            background: #eee;
            border: 1px solid #435da5;
            overflow: hidden;
            width: 100%;

            .progress {
                position: relative;
                display: block;
                background: #435da5;
                width: 0%;
                margin-left: 0%;
                height: 5px;
                // animation-name: animated;
                animation: animated 2s ease;
                // animation-duration: 2s;
            }
        }
    }


</style>
