<template>
<div class="home">
    <Nav/>
<div class="main">
    <div class="content">
        <h1 class="head">This is an app that allows you to <u>Search for words</u></h1>
        <div class="buttons">
            <a href="https://github.com/dinma-daniel/dictionary1">
            <button class="git"> view in Github</button>
            </a>
            <router-link to="/dictionary">
            <button class="app">Use app</button>
            </router-link>
        </div>
    </div>
    <div >
        <img class="imag" src="../assets/dictionary.png" >
    </div>
    </div>
</div>
</template>

<script>
import Nav from '../components/Nav.vue'

export default {
    name: "Home",
    components: {
        Nav
    },
    data(){
        return{
           
        }
    }
};
</script>

<style scoped>
:root {
    --color1: #313131;
    --color2: #414141;
    --color3: #525252;
    --color4: #ec625f;
}


.home {
    /* border: 1px solid red; */
    /* background-color: #313131; */
    margin: 0;
    padding: 0;
    height: 100vh;
    display: flex;
    flex-direction: column;
}

.main{
     /* border: 1px solid red; */
     margin: 3rem 0;
     display: flex;
}

.content {
    /* border: 1px solid red; */
    display: flex;
    flex-direction: column;
    width: 60%;
    margin-left: 4rem;
   margin-top: 8rem;
}

.imag{
    /* border: 1px solid red; */
    width: 100%;
    height: 100%;
   display: flex;
   justify-content: left;
}

.head {
    color: white;
    font-family: montserrat;
    font-size: 1.7rem;
    margin-bottom: 2.3rem;
    width: 100%;
}

u {
    /* font-family: robotto; */
    font-weight: 600;
    color: #ec625f;

}

button {
    border: none;
    padding: 1.5rem 3rem;
    border-radius: 10px;
    color: white;
    cursor: pointer;
}

.buttons {
    /* border: 1px solid red; */
    min-width: 400px;
    width: 40%;
    display: flex;
    justify-content: space-between;
}

.git {
    background-color: #525252;
    font-size: 1rem;
}

.app {
    background-color: #ec625f;
    font-size: 1rem;
}




@media (max-width: 900px) {

    .home{
        overflow-x: hidden;
        height: auto;
    }
    
.main{
    flex-direction: column;
}

.content{
    width: 80%;
    margin-top: 2rem;
    margin-left: 3.2rem;
}

.imag{
    margin-top: 8rem;
    width: 100%;
}


}

</style>
