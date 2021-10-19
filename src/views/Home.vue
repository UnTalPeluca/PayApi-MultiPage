<template>
  <div id="home">
    <section id="first-section">
      <img src="@/assets/home/desktop/illustration-phone-mockup.svg" alt="">
      <div class="content-wrapper">
        <h1 class="title">Start building with our APIs for absolutely free.</h1>
        <InputEmail/>
        <p>Have any questions? <router-link to="/contact"><span>Contact Us</span></router-link></p>
      </div>
    </section>
    <section id="second-section">
      <div class="section-wrapper">
        <div class="trademarks">
          <img src="@/assets/shared/desktop/tesla.svg" alt="">
          <img src="@/assets/shared/desktop/microsoft.svg" alt="">
          <img src="@/assets/shared/desktop/hewlett-packard.svg" alt="">
          <img src="@/assets/shared/desktop/oracle.svg" alt="">
          <img src="@/assets/shared/desktop/google.svg" alt="">
          <img src="@/assets/shared/desktop/nvidia.svg" alt="">
        </div>
      </div>
      <div class="content-wrapper">
        <h2 class="title">Who we work with</h2>
        <p>Today, millions of people around the world have successfully connected their accounts to apps they love using our API. We provide developers with the tools they need to create easy and accessible experiences for their users. </p>
        <router-link to="/about"><button>About Us</button></router-link>
      </div>
    </section>
    <section id="third-section">
      <div class="feature">
        <div id="img-implement">
          <img src="@/assets/home/desktop/illustration-easy-to-implement.svg" alt="">
        </div>
        <div class="content-wrapper">
          <h3 class="title">Easy to implement</h3>
          <p>Our API comes with just a few lines of code. You’ll be up and running in no time. We built our documentation page to integrate payments functionality with ease.</p>
        </div>
      </div>
      <div class="feature">
        <div id="img-simple">
          <img src="@/assets/home/desktop/illustration-simple-ui.svg" alt="">
        </div>
        <div class="content-wrapper">
          <h4 class="title">Simple UI & UX</h4>
          <p>Our pre-built form is easy to integrate in your app or website’s checkout flow and designed to optimize conversion. </p>  
        </div>
      </div>
    </section>
    <section id="fourth-section">
      <div class="feature-mini">
        <img src="@/assets/home/desktop/icon-personal-finances.svg" alt="">
        <div class="content-wrapper">
          <p class="title-mini">Personal Finances</p>
          <p class="description-mini">Consolidate financial data from multiple sources and categorize transactions up to 2 years of history. Analyze reports to reconcile activities in your account.</p>
        </div>
       </div>
       <div class="feature-mini">
        <img src="@/assets/home/desktop/icon-banking-and-coverage.svg" alt="">
        <div class="content-wrapper">
          <p class="title-mini">Banking & Coverage</p>
          <p class="description-mini">With our platform, you can speed up account onboarding and support ongoing payments for checking, savings, credit card, and brokerage accounts.</p>
        </div>
      </div>
      <div class="feature-mini">
      <img src="@/assets/home/desktop/icon-consumer-payments.svg" alt="">
      <div class="content-wrapper">
          <p class="title-mini">Consumer Payments</p>
          <p class="description-mini">It’s easier to set up secure bank payments with us through a flow designed with the user experience in mind. Customers could instantly authenticate their account.</p>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
import InputEmail from '../components/_inputEmail.vue'

export default {
  name: 'App',
  components:{
    InputEmail,
  }
}
</script>
<style scoped>
  .content-wrapper{
    width: clamp(327px, 80vw, 425px);
    margin: auto;
  }
  #first-section{
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
    top: -15px;
  }
  #first-section img{
    object-fit: contain;
    width: clamp(225px, 45vw, 275px);
    height: 100%;
    padding-left: 25px;
    padding-top: 20px;
  }
  #first-section .content-wrapper{
    position: relative;
    top: -25px;
  }
  #first-section p{
    font-family: 'Public Sans', sans-serif;
    padding-top: 24px;
    padding-bottom: 30px;
  }
  #first-section span{
    font-weight: bold;
    color: var(--text-color);
  }
   #first-section span:hover{
    opacity: 0.75;
  }
  #second-section{
    background-color: var(--bg-secondary);
    padding: 75px 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-image: url(../assets/shared/desktop/bg-pattern-circle.svg);
    background-repeat: no-repeat;
    background-position-x: center;
    background-position-y: -605px;
  }
  .trademarks {
    display: grid;
    grid-gap: 30px 0;
    grid-template-columns:repeat(auto-fit, minmax(150px,1fr));
    margin: auto;
    place-items: center;
    width: 327px;
  }
  .trademarks > img{
    filter: brightness(10);
    transform: scale(0.8);
  }
  .trademarks > img:nth-child(even){
    justify-self: end;
  }
  #second-section .title{
    color: white;
    padding-top: 50px;
    padding-bottom: 15px;
  }
  #second-section button{
    height: 48px;
    width: 129px;
    border-radius: 24px;
    border: 1px solid white;
    color: white;
    background-color: transparent;
    margin-top: 50px;
    font-size: 1.5rem;
  }
  #second-section button:hover{
    cursor: pointer;
    background-color: white;
    color: var(--bg-secondary);
  }
  #second-section p{
    color: var(--text-color-alt);
  }
  #third-section{
    padding-top: 100px;
    padding-bottom: 75px;
    display: flex;
    flex-direction: column;
    align-items: center;
    overflow: hidden;
  }
  #img-implement img{
    width: clamp(300px, 75vw, 375px);
    transform: scale(1.5);
    margin-left: 10%;
  }
  #third-section p{
    padding-top: 15px;
  }
  #img-simple img{
    width: clamp(300px, 75vw, 375px);
    transform: scale(1.4);
    margin-left: 5%;
    margin-top: 100px;
  }
  .feature:nth-child(2) .title{
    padding-top: 25px;
  }
  /* 4 */
  #fourth-section{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: auto;
    gap: 50px;
    padding-bottom:100px;
  }
  .title-mini{
    font-size: 1.8rem;
    line-height: 2.5rem;
    letter-spacing: -0.15px;
    font-weight: bold;
    color: var(--title-color);
    padding-top: 25px;
  }
  .description-mini{
    letter-spacing: -0.12px;
    line-height: 2.5rem;
    padding-top: 20px;
  }
@media screen and (min-width:768px) {
  .title{
    font-size: 4.8rem;
    line-height: 5.6rem;
    letter-spacing: -0.37px;
  }
  .content-wrapper{
    width: 573px;
  }
  #first-section p{
    padding-top: 0;
    padding-bottom: 50px;
  }
  .trademarks{
    width: 536px;
  }
  .trademarks > img:nth-child(even){
    justify-self: inherit;
  }
  .trademarks > img{
    transform: scale(1);
  }
  #second-section p{
    max-width: 456px;
    margin: auto;
  }
  #second-section{
    background-position-y: -580px;
  }
  #fourth-section{
    flex-direction: row;
    align-items: flex-start;
    gap: 0;
    justify-content: space-between;
    max-width: clamp(727px, 80vw, 1110px);
    padding-bottom:125px;
  }
  .feature-mini .content-wrapper{
    width: 227px;
  }
}
@media screen and (min-width:1280px) {
  .content-wrapper{
    width: 550px;
  }
  #first-section{
    flex-direction: row-reverse;
    justify-content: space-between;
    max-width: 1110px;
    margin: auto;
    top: 25px;
  }
  #first-section .content-wrapper{
    margin: 0;
    text-align: start;
    padding-top: 100px;
  }
  #first-section .input-email-wrapper{
    margin: 0;
  }
  #first-section .content-wrapper .title{
    font-size: 7.2rem;
  }
  #first-section img{
    width: 400px;
  }
  #first-section p{
    padding-left: 25px;
  }
  
  #second-section{
    flex-direction: row-reverse;
    justify-content: center;
    text-align: start;
    padding: 100px 0;
    background-position-x: calc(67% + -680px);
    background-position-y: -360px;
  }
  #second-section .title{
    padding: 0;
  }
  #second-section .content-wrapper p{
    padding-top: 25px;
    margin: 0;
  }
  #second-section button{
    margin-top: 30px;
  }
  #second-section .content-wrapper, .trademarks{
    width: 550px;
    margin: 0;
  }
  #third-section{
    max-width: 1110px;
    margin: auto;
    padding-top: 100px;
    padding-bottom: 50px;
  }
  #img-implement, #img-simple{
    width: 550px;
  }
  #img-implement img{
    margin-left: 0;
    padding-top: 20px;
    position: relative;
    right: 50px;
  }
  .feature{
    padding: 0;
  }
  .feature:nth-child(1){
    display: flex;
  }
  .feature:nth-child(1) .content-wrapper{
    padding-left: 25px;
  } 
  .feature:nth-child(2){
    display: flex;
    flex-direction: row-reverse;
    padding-top: 100px;
    padding-bottom: 150px;
  }
  .feature p{
    max-width:425px
  }
  #img-simple img{
    transform: scale(2);
  }
  #fourth-section .content-wrapper, #fourth-section p{
    width: 335px;
    text-align: center;
  }
  #home{
    background-image: url(../assets/shared/desktop/bg-pattern-circle.svg);
    background-repeat: no-repeat;
    background-position-x: calc(67% + 600px);
    background-position-y: 1450px;
  }
}
</style>