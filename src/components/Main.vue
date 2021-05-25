<template>
  <main>
    <div class="container tex-center pt-5">
     <div class="row">
        <Search
        v-for="record in records" :key="record.genre" :record="record"
        />
        <Record
         v-for="record in records" :key="record.title" :record="record"
        />

        </div>
     </div>
   

       
    
  </main>

</template>

<script>
import Record from '@/components/Record.vue'
import axios from 'axios';
import Search from './Search.vue';

export default {
  data(){
    return{
      records: [],
      axios,
      
    } 
  },
  components: { 
    Record,
    Search
  },
  
  name: 'Main',
  created(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then(res=> {
        console.log(res.data.response)     
        this.records = res.data.response
        
      })
      .catch(err => {
        console.log(err)
      })

  },

  /* computed:{
    filteredArr(){
      return this.records.filter(item => )
    }
  },  */
}

</script>

<style lang="scss" scoped>

@import '~bootstrap/scss/bootstrap';

main{
  background-color: #1e2d3b;
  height: 100%;
  width: 100%;
}

</style>