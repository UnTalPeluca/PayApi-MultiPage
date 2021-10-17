<template>
<div id="pricing">
    <p class="title">Pricing</p>
    <div class="plans-container">
        <div v-for="plan in plans" v-bind:key="plan.id" class="plan">
            <div class="plan-info">
                <h1 class="plan-name title">{{plan.name}}</h1>
                <p class="plan-description">{{plan.description}}</p>
                <p class="plan-price title">{{plan.price}}</p>
            </div>
            <div class="plan-features">
                <p class="plan-feature" :class="plan.features.includes(feature) ? 'feature-on' : '' " v-for="(feature, index) in features" :key="index">{{feature}}</p>
            </div>
            <router-link to="/contact"><button>Request Access</button></router-link>
        </div>
    </div>
</div>
</template>
<script>
export default {
    data(){
        return{
            plans: [
                {
                    "id":1,
                    "name": "Free Plan",
                    "description":"Build and test using our core set of products with up to 100 API requests",
                    "price": "$0.00",
                    "features": ["Transactions", "Auth", "Identity"]
                },
                {
                    "id":2,
                    "name": "Basic Plan",
                    "description":"Launch your project with unlimited requests and no contractual minimums",
                    "price": "$249.00",
                    "features": ["Transactions", "Auth", "Identity", "Investments", "Assets"]
                },
                {
                    "id":3,
                    "name": "Premium Plan",
                    "description":"Get tailored solutions, volume pricing, and dedicated support for your team",
                    "price": "$499.00",
                    "features": ["Transactions", "Auth", "Identity", "Investments", "Assets", "Liabilities", "Income"]
                }
            ],
            features:["Transactions", "Auth", "Identity", "Investments", "Assets", "Liabilities", "Income"],
        }
    }
}
</script>
<style scoped>
button{
    height: 48px;
    width: 168px;
    border-radius: 24px;
    border: 1px solid #36536B;
    color: #36536B;
    background-color: transparent;
    margin-top: 25px;
    font-size: 1.5rem;
}
.plan-description{
    display: none;
}
#pricing{
    font-family: 'Public Sans', sans-serif;
    padding-top: 25px;
    padding-bottom: 75px;
}
.plan-name{
    color: var(--primary-btn-normal);
    font-size: 2.4rem;
    padding-top: 50px;
}
.plan-price{
    padding-top: 75px;
    padding-bottom: 20px;
    font-size: 5.6rem;
    line-height: 7.2rem;
    letter-spacing: -0.43;
}
.plan-features{
    width: 327px;
    padding: 20px 0;
    margin: auto;
    border-top: 2px solid rgba(54, 83, 107, 0.1);
    border-bottom: 2px solid rgba(54, 83, 107, 0.1);
}
.plan-feature{
    text-align: start;
    margin-left: 40%;
    line-height: 32px;
    opacity: 0.5;
}
.feature-on{
    color: var(--title-color);
    opacity: 1;
    position: relative;
}
.feature-on::before{
    display: block;
    position: absolute;
    left: -30px;
    top:8px;
    transform: rotate(45deg);
    height: 10px;
    width: 4px;
    border-bottom: 2px solid #BA4270;
    border-right: 2px solid #BA4270;
    content: "";
}
@media screen and (min-width:768px) {
    .plans-container{
        display: flex;
        justify-content: space-between;
    }
    .plan-features{
        width: 223px
    }
    #pricing{
        padding-top: 100px;
        padding-bottom: 150px;
        width: clamp(690px, 90vw, 1110px);
        margin: auto;
    }
    .plan-description{
        display: block;
        max-width: 223px;
    }
}
@media screen and (min-width:1280px) {
    #pricing{
        text-align: start!important;
        padding-bottom: 100px;
    }
    .plan-description{
        display: block;
        max-width: 350px;
    }
    .plan-features{
        width: 350px;
    }
    .plan-feature{
        margin-left: 10%;
    }
}
</style>