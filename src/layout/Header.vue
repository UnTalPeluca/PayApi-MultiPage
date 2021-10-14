<template>
    <header>
        <router-link @click="isMenuOpen = false" to="/"><img src="@/assets/shared/desktop/logo.svg" alt="Logo"></router-link>
        <img @click="isMenuOpen=true" src="@/assets/shared/mobile/menu.svg" alt="">
        <div :class="isMenuOpen?'show-mobile-menu':'hide-mobile-menu'" id="nav-bar">
            <div id="nav-wrapper">
                <img @click="isMenuOpen = !isMenuOpen" src="@/assets/shared/mobile/close.svg" alt="close button">
                <router-link class="border-top" @click="isMenuOpen = false" to="/pricing">Pricing</router-link>
                <router-link @click="isMenuOpen = false" to="/about">About</router-link>
                <router-link @click="isMenuOpen = false" to="/contact">Contact</router-link>
            </div>
            <button @click="isMenuOpen = false" class="submit-button">Schedule a Demo</button>
        </div> 
    </header>
</template>
<script>
export default {
  name: 'Header',
  data(){
      return{
          isMenuOpen: false,
      }
  },
}
</script>
<style scoped>
header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 40px;
    max-width: clamp(327px, 80vw, 690px);
    margin: auto;
}
header > img:hover{
    cursor: pointer;
}
#nav-bar{
    position: fixed;
    top: 0;
    right: 0;
    background-color: var(--bg-secondary);
    width: 300px;
    font-size: 2rem;
    z-index: 1;
    height: 100vh;
    transition: transform 500ms ease-in-out;
    transform: translateX(0px);
    opacity: 0;
}
.show-mobile-menu{
    display: block;
    opacity: 1!important;
    transform: translateX(0)!important;
}
#nav-wrapper{
    display: flex;
    flex-direction: column;
    max-width: 250px;
    margin: auto;
    gap: 30px;
}
#nav-wrapper img{
    width: 22px;
    height: 22px;
    align-self: flex-end;
    margin-top: 40px;
    box-sizing: content-box;
}
#nav-wrapper img:hover{
    cursor: pointer;
}
.border-top{
    border-top: 1px solid rgba(151, 151, 151, 0.15);
    padding-top: 50px;
}
.submit-button{
    height: 48px;
    width: 250px;
    background-color: var(--primary-btn-normal);
    border: none;
    border-radius: 24px;
    color: white;
    font-size: 1.5rem;
    margin-top: 30px;
}
.submit-button:hover{
    background-color: var(--primary-btn-hover);
    cursor: pointer;
}
@media screen and (min-width:768px) {
    header{
        max-width: clamp(690px, 80vw, 1110px);
    }
    header > img, #nav-wrapper > img{
        display: none;
    }
    .border-top{
        border:0;
        padding: 0;
    }
    #nav-bar{
        position: static;
        transform: none;
        background-color: transparent;
        height: auto;
        width: auto;
        font-size: 1.5rem;
        display: flex;
        justify-content: space-between;
        width: 100%;
        opacity: 1;
    }
    #nav-bar a{
        color: inherit;
    }
    #nav-wrapper{
        flex-direction: row;   
        align-items: center;
        margin: 0 50px;
        max-width: 100%;
        gap: 50px;
    }
    .submit-button{
        width: 173px;
        margin: 0;
    }
}
@media screen and (min-width: 1280px) {

}
</style>