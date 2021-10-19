<template>
    <div id="contact">
        <p class="title">Submit a help request and we’ll get in touch shortly.</p>
        <div class="contact-content">
            <form>
                <label for="input-name"><input required ref="i1" placeholder="Name" name="name" id="input-name"></label>
                <small></small>
                <label for="input-email"><input required ref="i2" placeholder="Email Address" type="email" name="email" id="input-email"></label>
                <small></small>
                <label for="input-company"><input ref="i3" placeholder="Company Name" name="company" id="input-company"></label>
                <label for="input-title"><input ref="i4" placeholder="Title" name="title" id="input-title"></label>
                <label for="input-message"><textarea required ref="i5" placeholder="Message" name="message" id="input-message" cols="30" rows="10"></textarea></label>
                <small></small>
                <div class="control-group">
                    <label class="control control-checkbox">
                        <input type="checkbox" checked="checked" />
                        <div class="control_indicator"></div>
                        <span>Stay up-to-date with company announcements and updates to our API</span>
                    </label>
                </div>
                <button @click="submit">Submit</button>
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
<script>
export default {
    methods: {
        submit: function (event){
            // Inputs
            const name = this.$refs.i1
            const email = this.$refs.i2
            const message = this.$refs.i5
            // Check if empty
            function isEmpty(value){
                return value === ""
            }
            // Check length
            function hasEnoughLength(length){
                return length >= 5
            }
            function isValidEmail(email) {
                const pattern = /^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:.[a-zA-Z0-9-]+)*$/
                return pattern.test(email)
            }
            // Errors
            function showError(input, msg){
                const parent = input.parentElement
                const errorMsg = parent.nextElementSibling
                parent.style.borderBottomColor = "rgba(255, 0, 0, 0.25)"
                errorMsg.textContent = msg
            }
            function clearError(input){
                const parent = input.parentElement
                const errorMsg = parent.nextElementSibling
                parent.style.borderBottomColor = "rgba(54, 83, 107, 0.25)"
                errorMsg.textContent = ""
                document.documentElement.style.setProperty(`--placeholder${input.name}`, '#36536B');
            }
            // Check Function
            let isValid = true
            event.preventDefault()
            function checkInput(input, isEmail){
                if(isEmpty(input.value)){
                    showError(input, "This field can't be empty")
                    document.documentElement.style.setProperty(`--placeholder${input.name}`, '#FF0000');
                    isValid = false
                }else if(isEmail && !isValidEmail(input.value)){
                    showError(input, "You must enter a valid email")
                    isValid = false
                }
                else if (!hasEnoughLength(input.value.length)){
                    showError(input, "Must be at least 5 characters")
                    document.documentElement.style.setProperty(`--placeholder${input.name}`, '#FF0000');
                    isValid = false
                }
                else{
                    clearError(input)
                    event.preventDefault()
                }
            }
            checkInput(name)
            checkInput(email, true)
            checkInput(message)
            if (isValid){
                this.$router.push('/')
            }
        }
    }
}
</script>
<style scoped>
    form button:hover{
        background-color: var(--bg-secondary);
        color: white;
        cursor: pointer;
    }
    small{
        height: 0;
        color: rgba(255, 0, 0, 0.5);
        font-size: 11px;
        letter-spacing: -0.08px;
        text-align: start;
        padding-left: 17px;
        position: relative;
        top: -2.5px;
    }
    #input-name::after{
        content: "hola";
        height: 50px;
        width:50px;
        color: red;
    }
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
        position: relative;
    }
    textarea{
        resize: none;
    }
    input::placeholder, textarea::placeholder{
        opacity: 0.5;
        color: #36536B;
    }
    #input-name::placeholder{
        color: var(--placeholdername);
    }
    #input-email::placeholder{
        color: var(--placeholderemail);
    }
    #input-message::placeholder{
        color: var(--placeholdermessage);
    }
    label:nth-child(7){
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
    /* checkbox */
    .control-group label{
        border-bottom: 0;
    }
    .control-group{
        padding-top: 10px;
    }
    .control {
    font-family: arial;
    display: block;
    position: relative;
    padding-left: 30px;
    margin-bottom: 5px;
    padding-top: 0px;
    cursor: pointer;
    font-size: 16px;
    }
    .control-group span{
        text-align: start;
        position: absolute;
        width: 275px;
        font-size: 1.5rem;
        left: 50px;
        top: 10px;
        line-height: 2.5rem;
        color: #36536B;
        letter-spacing: -0.12px;
        font-family: 'Public Sans', sans-serif;
    }
    
    .control input {
        position: absolute;
        z-index: -1;
        opacity: 0;
    }
.control_indicator {
    position: absolute;
    top: 22.5px;
    left: 0;
    height: 24px;
    width: 24px;
    background: rgba(151, 151, 151, 1);
    border: 0px solid #000000;
    border-radius: 0px;
}
.control input:checked ~ .control_indicator {
    background: #BA4270;
}
.control:hover input:not([disabled]):checked ~ .control_indicator,
.control input:checked:focus ~ .control_indicator {
    background: #BA4270;
}
.control input:disabled ~ .control_indicator {
    background: #e6e6e6;
    opacity: 0.6;
    pointer-events: none;
}
.control_indicator:after {
    box-sizing: unset;
    content: '';
    position: absolute;
    display: none;
}
.control input:checked ~ .control_indicator:after {
    display: block;
}
.control-checkbox .control_indicator:after {
    left: 9px;
    top: 5px;
    width: 4px;
    height: 9px;
    border: solid #ffffff;
    border-width: 0 2px 2px 0;
    transform: rotate(45deg);
}
.control-checkbox input:disabled ~ .control_indicator:after {
    border-color: #7b7b7b;
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
    .control-group span{
        width: 400px;
    }
    .title{
        font-size: 4.8rem;
        width: 530px;
        line-height: 5.6rem;
    }
    label, form{
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