<template>
    <footer>
        <div class="footer-wrapper">
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
        </div>
    </footer>
</template>
<style scoped>
router-link{
    color: red;
}
footer{
    background-color: var(--bg-secondary);
    background-image: url(../assets/shared/desktop/bg-pattern-circle.svg);
    background-repeat: no-repeat;
    background-position-x: center;
    background-position-y: -45%;
}
.footer-wrapper{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 40px;
    padding: 40px 0;
    margin: auto;
}
.footer-wrapper > img{
    filter: brightness(10);
}
.footer-links{
    display: flex;
    flex-direction: column;
    gap: 20px;
}
.footer-social{
    margin: auto;
    display: flex;
    align-items: center;
    gap: 20px; 
}
.footer-social > a{
    display: flex;
    align-items: center;
}
@media screen and (min-width:768px) {
    .footer-wrapper{
        max-width: clamp(690px, 90vw, 1110px);
        padding: 0;
        flex-direction: row;
        height: 100px;
    }
    .footer-links{
        flex-direction: row;
        align-items: center;
        padding: 0;
        padding-left: 20px;
        gap: 45px;
    }
    .footer-social{
        margin: 0;
        margin-left: auto;
    }
}
</style>