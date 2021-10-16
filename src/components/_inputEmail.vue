<template>
    <div class="input-email-wrapper">
        <slot></slot>
        <form action="">
            <input type="email" name="email-input" placeholder="Enter email address">
            <button class="submit-button">Schedule a Demo</button>
        </form>
    </div>
</template>
<script>
export default {
    name:'inputEmail',
    }
</script>
<style scoped>
    .input-email-wrapper{
        width: 327px;
        margin: auto;
    }
    input{
        border: none;
        outline: none;
        height: 48px;
        width: 327px;
        background-color: white;
        border-radius: 24px;
        padding-left: 25px;
        margin-bottom: 16px;
        margin-top: 24px;
        color: red;
    }
    input::placeholder{
        font-family: 'Public Sans', sans-serif;
        font-weight: bold;
        font-size: 1.5rem;
        color: rgba(54, 83, 107, 0.5);
    }
    .submit-button{
        height: 48px;
        width: 327px;
        background-color: var(--primary-btn-normal);
        border: none;
        border-radius: 24px;
        color: white;
        font-size: 1.5rem;
    }
    .submit-button:hover{
        background-color: var(--primary-btn-hover);
        cursor: pointer;
    }
@media screen and (min-width:768px) {
    form{
        padding-top: 10px;
        display: flex;
        align-items: center;
        width: 445px;

    }
    input{
        border-top-right-radius: 0;
        border-bottom-right-radius: 0;
    }
    .submit-button{
        position: relative;
        right: 20px;
        top: 4px;
        width: 50%;
    }
}
</style>