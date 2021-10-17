<template>
    <div id="contact">
        <p class="title">Submit a help request and we’ll get in touch shortly.</p>
        <div class="contact-content">
            <form>
                <label for="name"><input placeholder="Name" name="name" id="input-name"></label>
                <label for="email"><input placeholder="Email Address" type="email" name="email" id="input-email"></label>
                <label for="company"><input placeholder="Company Name" name="company" id="input-company"></label>
                <label for="title"><input placeholder="Title" name="title" id="input-title"></label>
                <label for="message"><textarea placeholder="Message" name="message" id="input-message" cols="30" rows="10"></textarea></label>
                <div class="suscribe">
                    <input type="checkbox" name="suscribe" id="input-suscribe">
                    <p>Stay up-to-date with company announcements and updates to our API</p>
                </div>
                <button type="submit">Submit</button>
            </form>
            <section>
                <p class="title">Join the thousands of innovators already building with us</p>
                <div class="trademarks">
                    <img src="@/assets/shared/desktop/tesla.svg" alt="">
                    <img src="@/assets/shared/desktop/microsoft.svg" alt="">
                    <img src="@/assets/shared/desktop/hewlett-packard.svg" alt="">
                    <img src="@/assets/shared/desktop/oracle.svg" alt="">
                    <img src="@/assets/shared/desktop/google.svg" alt="">
                    <img src="@/assets/shared/desktop/nvidia.svg" alt="">
                </div>
            </section>
        </div>
    </div>
</template>
<style scoped>
    p{
        text-align: center;
        padding-top: 50px;
        width: clamp(327px, 70vw, 573px);
    }
    form{
        display: flex;
        flex-direction: column;
    }
    label{
        height: 66px;
        border-bottom: 2px solid rgba(54, 83, 107, 0.25);
        display: flex;
        align-items: center;
        width: clamp(327px, 70vw, 573px);
        margin: auto;
    }
    input, textarea{
        height: 25px;
        background:transparent;
        width: 90%;
        margin-left: 5%;
        outline: none;
        border: none;
        font-family: 'Public Sans', sans-serif;
        color: #36536B;
        padding-top: 10px;
    }
    textarea{
        resize: none;
    }
    input::placeholder, textarea::placeholder{
        opacity: 0.5;
        color: #36536B;
    }
    label:nth-child(5){
        height: 110px;
        padding-top: 10px;
    }
    #input-message{
        height: 80px;
    }
    form{
        width: clamp(327px, 70vw, 573px);
        margin: auto;
        padding-bottom: 50px;
    }
    .suscribe{
        display: flex;
        align-items: center;
        justify-content: flex-start;
        width: clamp(327px, 80vw, 573px);
        padding-top: 20px;
        margin: auto;
        gap: 30px;
    }
    .suscribe input, .suscribe p{
        width: auto;
        padding: 0;
        text-align: start;
        color: #36536B;
    }
    .suscribe input{
        transform: scale(1.5);
        margin: 0;
        border: none;
        outline: none;
        box-shadow: none;
    }
    section p{
        font-size: 2.4rem;
        opacity: 0.75;
        padding: 25px 0;
    }
    .trademarks{
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: space-between;
        gap: 25px;
        width: 310px;
        margin: auto;
        padding-bottom: 75px;
    }
    .trademarks img{
        transform: scale(0.8);
    }
    form button{
        height: 48px;
        width: 129px;
        border-radius: 24px;
        border: 1px solid var(--title-color);
        background-color: transparent;
        font-size: 1.5rem;
        margin-top: 20px;
    }
@media screen and (min-width:768px) {
    .title{
        font-size: 4.8rem;
        width: 530px;
        line-height: 5.6rem;
    }
    label, .suscribe, form{
        width: 445px;
    }
    section .title{
        width: 440px;
        font-size: 2.4rem;
        line-height: 3.2rem;
    }
    .trademarks{
        width: 540px;
        padding-top: 25px;
        padding-bottom: 125px;
    }
    .trademarks img{
        transform: scale(1);
    }
}
@media screen and (min-width:1280px) {
    .contact-content{
        display: flex;
        margin: auto;
        width: 1110px;
        justify-content: space-between;
    }
    form{
        margin: 0;
    }
    section{
        padding-top: 110px;
    }
    #contact > .title{
        width: 1110px;
        text-align: start;
        padding-right: 500px;
    }
}
</style>