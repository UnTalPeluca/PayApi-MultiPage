<template>
  <div id="about">
    <h1 class="title">We empower innovators <span>by delivering access to the financial system</span></h1>
    <section id="first-section">
      <article>
        <p class="title">Our Vision</p>
        <p>Our main goal is to build beautiful consumer experiences along with developer-friendly infrastructure. The result is an intelligent tool that gives everyone the ability to create amazing products that solve big problems. We are deeply focused on democratizing financial services through technology.</p>
      </article>
      <article>
        <p class="title">Our Business</p>
        <p>At the core of our platform is the technical infrastructure APIs that connect consumers. Our innovative product provides key insights for businesses and individuals, as well as robust reporting for traditional financial institutions and developers.</p>
      </article>
    </section>
    <div id="image-team"></div>
    <section id="second-section">
      <div class="stat">
        <p class="stat-title">Team Members</p>
        <p class="stat-value">300+</p>
      </div>
      <div class="stat">
        <p class="stat-title">Offices in the US</p>
        <p class="stat-value">3</p>
      </div>
      <div class="stat">
        <p class="stat-title">Transactions analyzed</p>
        <p class="stat-value">10M+</p>
      </div>
    </section>
    <section id="third-section">
      <article>
        <p class="title">The Culture</p>
        <p>We strongly believe there's always an opportunity to learn from each other outside of day-to-day work, whether it's company-wide offsites, internal hackathons, or co-worker meetups. We always value cross-team collaboration and diversity of thought, no matter the job title.</p>
      </article>
      <article>
        <p class="title">The People</p>
        <p>We're all passionate about building a more efficient and inclusive financial infrastructure together. At PayAPI, we have diverse backgrounds and skills.</p>
      </article>
    </section>
  </div>
</template>
<style scoped>
#about{
  padding-top: 50px;
}
article{
  width: clamp(315px, 60vw, 690px);
  margin: auto;
}
.title{
  width: 315px;
  line-height: 3.6rem;
}
span{
  display: block;
}
article .title{
  font-size: 2.4rem
}
#first-section{
  padding-top: 50px;
  padding-bottom: 50px;
  display: flex;
  flex-direction: column;
  gap: 50px;
}
#image-team{
  width: 100%;
  height: 300px;
  background-image: url(../assets/about/mobile/image-team-members.jpg);
  background-repeat: no-repeat;
  background-size: cover;
}
#second-section{
  padding: 20px 0;
  border-top: 1px solid rgba(54, 83, 107, 0.25);
  border-bottom: 1px solid rgba(54, 83, 107, 0.25);
  margin-top: 50px;
  display: flex;
  flex-direction: column;
  gap: 25px;
}
.stat-value{
  font-family: 'DM Serif Display', serif;
  font-size: 5.6rem;
  line-height: 7.2rem;
  letter-spacing: -0.43px;
  color: #BA4270;
}
#third-section{
  padding-top: 50px;
  padding-bottom: 50px;
  display: flex;
  flex-direction: column;
  gap: 50px;
}
@media screen and (min-width:768px) {
.title{
  width: clamp(573px, 60vw, 730px);
  font-size: 4.8rem;
  line-height: 5.6rem;
}
article{
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  width: clamp(690px, 85vw, 920px);
  text-align: start;
}
article p{
  width: clamp(456px, 60vw, 920px);
}
article .title{
  text-align: start;
  width: 230px;
  font-size: 3.2rem;
  line-height: 4rem;
  margin: 0;
}
#image-team{
  background-image: url(../assets/about/tablet/image-team-members.jpg);
  height: 267px;
}
#second-section{
  flex-direction: row;
  justify-content: space-between;
  width: clamp(690px, 85vw, 1110px);
  margin-left: auto;
  margin-right: auto;
  text-align: start;
  border:none;
}
.stat{
  width: 223px;
  border-top: 1px solid rgba(54, 83, 107, 0.25);
  border-bottom: 1px solid rgba(54, 83, 107, 0.25);
  padding: 20px 0;
}
}
@media screen and (min-width:1280px) {
  #about > .title{
    text-align: start;
    width: 920px;
    padding-right: 250px;
    padding-top: 20px;
    font-size: 5.6rem;
  }
  #first-section{
    padding-bottom: 100px;
  }
  #image-team{
    background-image: url(../assets/about/desktop/image-team-members.jpg);
    height: 500px;
  }
  .stat{
    width: 350px;
  }
  article{
    width:920px;
  }
  article p{
    width: 635px;
  }
  #about{
    background-image: url(../assets/shared/desktop/bg-pattern-circle.svg);
    background-repeat: no-repeat;
    background-position-x: calc(30% + -700px);
    background-position-y: 525px;
  }
}
</style>