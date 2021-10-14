<template>
    <footer>
        <img src="@/assets/shared/desktop/logo.svg" alt="Logo">
        <div class="footer-links">
            <router-link class="router" to="/pricing">Pricing</router-link>
            <router-link class="router" to="/about">About</router-link>
            <router-link class="router" to="/contact">Contact</router-link>
        </div>
        <div class="footer-social">
            <a href="#"><img src="@/assets/shared/desktop/facebook.svg" alt="Logo"></a>
            <a href="#"><img src="@/assets/shared/desktop/twitter.svg" alt="Logo"></a>
            <a href="#"><img src="@/assets/shared/desktop/linkedin.svg" alt="Logo"></a>
        </div>
    </footer>
</template>
<style scoped>
router-link{
    color: red;
}
footer{
    background-color: var(--bg-secondary);
    padding: 50px 0;
    background-image: url(../assets/shared/desktop/bg-pattern-circle.svg);
    background-repeat: no-repeat;
    background-position-x: center;
    background-position-y: -45%;
}
footer > img{
    filter: brightness(10);
}
.footer-links{
    padding-top: 25px;
    display: flex;
    flex-direction: column;
    gap: 20px;
    padding-bottom: 40px;
}
.footer-social{
    margin: auto;
    display: flex;
    justify-content: center;
    gap: 20px; 
}
</style>