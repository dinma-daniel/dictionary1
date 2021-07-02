<template>
    <div class="search__container">
        <input class="search__bar" type="text" v-model="name">
    
        <button class="btn" @click="getSearch(name)">Search</button>
    </div>
</template>

<script>
export default {
    name: 'Search',
    data(){
        return{
            name: ''
        }
    },
  props: {
      getSearch: Function
  }
}
</script>

<style scoped>
.search__bar{
    padding: 1.5rem 6rem;
    border-radius: 10px 0 0 10px;
    margin: 0 auto;
    flex: 0.8;
    background-color: #FFC996;
    border: none;
    font-size: 1rem;
    font-weight: 600;
}

.search__container{
    /* border: 1px solid red; */
    width: 100%;
    margin: 0 auto;
    display: flex;
    margin-bottom: 1.5rem;
    
}

.btn{
    padding: 1.5rem 0;
    border-radius: 0 10px 10px 0;
    border: 1px solid #FFC996;
     flex: 0.2;
     background-color: sandybrown;
}
</style>