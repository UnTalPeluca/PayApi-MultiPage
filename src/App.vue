<template>
  <Header/>
  <router-view/>
  <div class="footer-input">
    <p class="title">Ready to start?</p>
    <InputEmail/>
  </div>
  <Footer/>
</template>
<script>
import Header from './layout/Header.vue'
import InputEmail from './components/_inputEmail.vue'
import Footer from './layout/Footer.vue'
export default {
  name: 'App',
  components:{
    Header,
    InputEmail,
    Footer,
  },
  watch: {
    $route(to, from) {
      let body = document.querySelector("body")
      if(to.name == "Home"){
        body.classList.remove("bg-pages")
      }else{
        body.classList.add("bg-pages")
      }
    }
  }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=Public+Sans:wght@400;700&display=swap');
/* font-family: 'DM Serif Display', serif;
font-family: 'Public Sans', sans-serif;*/
:root{
  --bg-primary:rgb(237,243,248);
  --bg-secondary:rgb(27, 38, 47);
  --title-color: rgb(54, 83, 107);
  --primary-btn-normal:rgb(186, 66, 112);
  --primary-btn-hover:rgb(218, 109, 151);
  --primary-btn-disabled:rgba(186, 66, 112, 0.1);
  --text-color: rgb(108, 130, 148);
  --text-color-alt: rgba(251, 252, 254, 0.7);
  --placeholdername: #36536B;
  --placeholderemail: #36536B;
  --placeholdermessage: #36536B;
}
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html{
  font-size: 62.5%;
  text-align: center;
  scroll-behavior: smooth;
}
body{
  background-color: var(--bg-primary);
  font-size: 1.5rem;
  line-height: 2.8rem;
  color: var(--text-color);
  background-image: url(./assets/shared/desktop/bg-pattern-circle.svg);
  background-repeat: no-repeat;
  background-position-x: center;
  background-position-y: -550px;
}
.bg-pages{
  background-position-x: calc(67% + 325px);
  background-position-y: -650px;
}
a{
  color: var(--text-color-alt);
  text-decoration: none;
  font-family: 'Public Sans', sans-serif;
  font-weight: bold;
}
#app{
  font-family: 'Public Sans', sans-serif;
}
button{
  font-family: 'Public Sans', sans-serif;
  font-weight: bold;
  letter-spacing: 0.12px;    
}
.title{
  font-family: 'DM Serif Display', serif;
  font-size: 3.2rem;
  font-weight: normal;
  line-height: 3.6rem;
  letter-spacing: -0.25px;
  text-align: center;
  margin: auto;
  color: #36536B;
}
Footer{
  margin-top: 75px;
}
@media screen and (min-width:768px) {
  .title{
    font-size: 5.6rem;
    letter-spacing: -0.37px;
    padding-bottom: 25px;
  }
  .bg-pages{
    background-position-x: calc(67% + 520px);
    background-position-y: -475px;
  }
}
@media screen and (min-width:1280px) {
  body{
    background-position-x: calc(67% + 400px);
    background-position-y: -200px;
  }
  .bg-pages{
    background-position-x: calc(67% + 350px);
    background-position-y: -510px;
  }
  body p, .title{
      text-align: start;
  }
  .footer-input{
    max-width: 1110px;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .footer-input > *{
    padding: 0;
  }
  .footer-input .title{
    margin: 0;
    margin-right: 225px;
  }
}
</style>
