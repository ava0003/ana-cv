<template>
    <div class="aboutme-wrapper">
      <div class="title-section">
        About <span>Me</span>
      </div>
      <div class="main-section">
          <div class="left-section">
            <div class="left-section-title">CREATIVITY BLEEDS FROM THE PEN OF INSPIRATION.</div>
            <div class="left-section-description">
              <p>I am your Brand Consultant having 8+ years of experience in this field provides complete
                range of marketing materials and branding solution to any industry as well as corporate
                clients maintaining their reputation and increasing the brand awareness using PR & other
                print media & online marketing activities.
              </p>
            </div>
            <ul class="left-section-personal-info-list">
              <li class="name"><b>Full Name : </b> Ana Villena</li>
              <li class="age">Age : 28 Years</li>
              <li class="lang">Language : Spanish, French, English </li>
              <li class="phone">Phone N : +34 663054821 / +33 0766512422</li>
              <li class="email">Email : anavillenaa@gmail.com</li>
              <li class="address">Address : Toulouse</li>
            </ul>
          </div>
          <div class="right-section">
            <ProgressBar item="HTML" percentage="30"/>
            <ProgressBar item="JAVASCRIPT" percentage="20"/>
            <ProgressBar item="CSS" percentage="40"/>
            <ProgressBar item="PYTHON" percentage="50"/>
          </div>
      </div>
      <div class="card-section">
          <Card title="Graphics Design" description="Develop the Visual Identity of Your Business"/>
          <Card title="Web Design" description="Connect with your users, not just your business"/>
          <Card title="Development" description="We develop the visual identity of your business"/>
          <Card title="Seo Friendly" description="Taking your site at the top of Google's ranking"/>
          <!-- <div class="card1">CARD 1</div>
          <div class="card2">CARD 2</div>
          <div class="card3">CARD 3</div>
          <div class="card4">CARD 4</div> -->
      </div>

    </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import ProgressBar from '../widgets/ProgressBar.vue'
import Card from '../widgets/Card.vue'
@Options({
  props: {},
  components: {
    ProgressBar,
    Card
  }
})
export default class AboutMe extends Vue {

}
</script>

<style lang="less" scoped>

  @spacer: 50px;
  @2spacer: @spacer * 2;
  @4spacer: @spacer * 4;


.aboutme-wrapper {
  position: relative;
  display: flex;
  flex-direction: column;
  // border: 0px 1px 1px 1px solid black;
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

          .left-section-description {
            background-color: white;
            width: 100%;
            text-align: left;
            color:rgb(75, 74, 74);
            font-weight: bold;
            font-size: 0.8 em;
            letter-spacing: 0.01rem;
          }
          .left-section-personal-info-list {
            background-color: white;
            width: 100%;
            text-align: left;
            color:rgb(75, 74, 74);
            font-size: 0.8 em;
            letter-spacing: 0.01rem;
            list-style-type: none;
            padding: 0;
            margin: 0;

            .name, .age, .lang, .phone, .email, .address {
              margin-top: 2.5%;
            }
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
