<template>
<div class="home">
    <Nav/>
<div class="main">
    <div class="content">
        <h1 class="head">This is an app that <em>generates new words</em> everytime</h1>
        <div class="buttons">
            <button class="git"> view in Github</button>
            <router-link to="/dictionary">
            <button class="app">Use app</button>
            </router-link>
        </div>
    </div>
    <div class="imag">
        <img :src="image" >
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
            image: '../assets/logo.png'
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
    background-color: var(--color1);
    margin: 0;
    padding: 0;
    height: 100vh;
    display: flex;
    flex-direction: column;
}

.main{
     /* border: 1px solid red; */
     margin: 8rem 0;
     display: flex;
}

.content {
    /* border: 1px solid red; */
    display: flex;
    flex-direction: column;
    width: 50%;
    justify-content: center;
    margin: 0 4rem;
}

.head {
    color: white;
    font-family: montserrat;
    font-size: 1.7rem;
    margin-bottom: 2.3rem;
    width: 80%;
}

em {
    font-family: josefinSlab;
    font-weight: lighter;
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

.imag{
    width: 200px;
}
</style>
