<template>
    <div class="experience-wrapper">
      <div class="title-section">
        My <span>Experience</span>
      </div>
      <div class="main-section">
          <div class="left-section">
            <div class="left-section-title">EDUCATION</div>
            <div class="timeline">
                <ul>
                    <li>
                        <span>Date 1</span>
                            <div class="content">
                                <h3>TITLE</h3>
                                <p>Description</p>
                            </div>
                    </li>
                    <li>
                        <span>Date 2</span>
                            <div class="content">
                                <h3>TITLE</h3>
                                <p>Description</p>
                            </div>
                    </li>
                    <li>
                        <span>Date 3</span>
                            <div class="content">
                                <h3>TITLE</h3>
                                <p>Description</p>
                            </div>
                    </li>
                </ul>
            </div>

          </div>
          <div class="right-section">
            <div class="right-section-title">EXPERIENCE</div>
            <ProgressBar item="HTML" percentage="30"/>
            <ProgressBar item="JAVASCRIPT" percentage="20"/>
            <ProgressBar item="CSS" percentage="40"/>
            <ProgressBar item="PYTHON" percentage="50"/>
          </div>
      </div>
      <div class="card-section">
          <Card title="XXX" description="Projects"/>
          <Card title="XXX" description="Clients"/>
          <Card title="XXX" description="Countries"/>
          <Card title="XXX" description="Awords"/>
      </div>

    </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Card from '../widgets/Card.vue'
@Options({
  props: {},
  components: {
    Card
  }
})
export default class Experience extends Vue {

}
</script>

<style lang="less" scoped>

  @spacer: 50px;
  @2spacer: @spacer * 2;
  @4spacer: @spacer * 4;


.experience-wrapper {
  position: relative;
  display: flex;
  flex-direction: column;
  height: calc(100vh - @2spacer);
  padding: 0;
  margin : @spacer;
  background-color: white;
  color: black;

    .title-section{
        background-color: white;
        flex-basis : 10%;
        width: 100%;
        text-align: center;
        color:#222;
        font-weight: bold;
        font-size: 2em;
        letter-spacing: 0.01rem;
        margin: 2%;
    }
    .title-section span{
      color: #435da5;
    }

    .main-section{
        position: relative;
        flex-basis : 50%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        width: 100%;
        padding: 0;
        margin : 0;
        color: black;

        .left-section, .right-section{
            position: relative;
            height: 100% ;
            flex-basis : 50%;
            margin: 2%;
        }

        .left-section {
          position: relative;
          display: flex;
          flex-direction: column;
          align-items: center;
          

            .left-section-title {
                background-color: white;
                width: 100%;
                text-align: left;
                color:#222;
                font-weight: bold;
                font-size: 1.1em;
                font-weight: 800;
                letter-spacing: 0.01rem;
            }
        
            .timeline{
                width:100%;

            }
            .timeline ul{
                list-style-type:none;
                border-left:2px solid #111;
                padding:10px 5px;
            }
            .timeline ul li{
                padding:20px 20px;
                position:relative;
            }
            .timeline ul li span{
                display:inline-block;
                padding:2px 5px;
                font-size:15px;
                text-align:center;
            }
            .timeline ul li .content h3{
                color:#435da5;
                font-size:17px;
                padding-top:5px;
            }
            .timeline ul li .content p{
                padding:5px 0px 15px 0px;
                font-size:15px;
            }
            .timeline ul li:before{
                position:absolute;
                content:'';
                width:10px;
                height:10px;
                background-color:#435da5;
                border-radius:50%;
                left:-11px;
                top:28px;
            }
                    
        }
    }


    .card-section{
        position: relative;
        flex-basis : 40%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        flex-wrap: no-wrap;
        padding: 0;
        margin : 0;
        height: 100%;

        // .card1, .card2, .card3, .card4{
        //     position: relative;
        //     border: 1px solid black;
        //     flex-basis : 25%;
        //     height: 100% ;
        //     text-align: center;
        // }
    }
}


</style>
