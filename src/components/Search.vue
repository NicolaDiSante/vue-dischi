<template>
  <div class="genre-box text-center">
    <button @click="toggle"> Generi </button>
    <div 
    
    :class=" active ? 'dropdown' : null "></div>
  </div>
</template>

<script>

export default {
  name: 'Search',
  props:{
    record: Object
  },
  data(){
    return {
      active: false
    }
  },
  methods:{
    toggle(){
      this.active = !this.active;
      console.log(this.records)
  } 
  }
  
}

</script>

<style lang="scss" scoped>

.genre-box{
  position: relative;
}


.dropdown{
  position: absolute;
  height: 150px;
  width: 150px;
  background-color: white;
  top: 20;
  right: 45%;
}

</style>