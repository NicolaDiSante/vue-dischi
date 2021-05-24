<template>
  <main>
    <div class="container tex-center pt-5">
     <div class="row">
     
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

export default {
  data(){
    return{
      records: [],
      axios,
    } 
  },
  components: { 
    Record
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
}

</script>

<style lang="scss" scoped>

@import '~bootstrap/scss/bootstrap';

main{
  background-color: #1e2d3b;
  height: calc(100vh - 60px);
  width: 100%;
}

</style>