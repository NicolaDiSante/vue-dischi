<template>
  <div id="app">

    <Header />
    <Main/>
    

  </div>
</template>

<script>

import Header from './components/Header.vue';
import Main from './components/Main.vue';


export default {
  name: "App",
  components: {
    Header,
    Main,
   
    
  },
  data(){
    return{
      
    }
  },
};
</script>

<style lang="scss">

*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

</style>
