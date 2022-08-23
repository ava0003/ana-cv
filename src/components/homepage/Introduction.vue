<template>
    <div class="introduction-wrapper">
      <div class="left-section">
        <div class="photo">
        </div>
      </div>
      <div class="right-section">
          <div class="description-wrapper">
              <div class="name">Ana Villena</div>
              <div class="job">- I am a Data Analyst</div>
              <div class="welcome_msg">Welcome to my site</div>
              <div class="buttons">
                <div class="left-button"> Download CV </div>
                <div class="right-button"> More Info</div>
              </div>
          </div>
      </div>

    </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {},
  components: {
  }
})
export default class Introduction extends Vue {

}
</script>

<style lang="less" scoped>

  @spacer: 50px;
  @2spacer: @spacer * 2;
  @4spacer: @spacer * 4;


.introduction-wrapper {
  position: relative;
  display: flex;
  border: 1px solid black;
  height: calc(100vh - @2spacer);
  padding: 0;
  margin : @spacer;
  background-color: white;
  color: black;

  .left-section, .right-section{
      position: relative;
      display: inline-flex;
      width: 50%;
  }

  .left-section{
    background-color: #191a1e;
    padding : 50px;

    .photo{
      position: absolute;
      height: 74%;
      width: 64%;
      top: calc(50% - 37%);
      left: calc(50% - 32%);
      background-image: url("@/assets/img/ana_profile.jpg");
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
    }
  }
  .right-section{
      background-color: white;

      .description-wrapper{
        position: relative;
        display: flex;
        flex-direction: column;
        flex-wrap: nowrap;
        column-gap : 0.2rem;
        padding: 0;
        width: 100%;
        align-items: center;
        justify-content: center;

        .name{
          position: relative;
          color:#435da5;
          font-family: "Quicksand";
          font-weight: bold;
          font-size: 2em;
          letter-spacing: 0.01rem;
      }
        .job{
          position: relative;
          color:#222;
          font-family: "Quicksand";
          font-size: 1.3em;
          letter-spacing: 0.01rem;
        }

        .welcome_msg{
          position: relative;
          margin-top: 5%;
          color:#222;
          font-family: "Quicksand";
          font-size: 1em;
          letter-spacing: 0.01rem;
        }
        .buttons{
          position: relative;
          display: flex;
          flex-direction: row;
          margin-top: 5%;
          gap: 5px;

          .left-button, .right-button {
            background-color: #222;
            border-radius: 4px;
            box-sizing: border-box;
            color: #fff;
            cursor: pointer;
            display: inline-block;
            font-family: "Farfetch Basis","Helvetica Neue",Arial,sans-serif;
            font-size: 0.8em;
            font-weight: 400;
            line-height: 1;
            padding: 9px 20px 8px;
            text-align: center;
          }
          .left-button{
            background-color: #222;
            color: #fff;
            border-style: none;
          }
          .right-button {
            background-color: #fff;
            color: #222;
            border-style: solid;
          }

        }
    }

  }
}


</style>
