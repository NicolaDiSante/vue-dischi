<template>

  
  <div class="box col-lg-2 text-center text-uppercase">
    
   <div class="row">

    <img class="col-lg-12" :src="record.poster" alt="">
    <h2 class="col-lg-12"> {{ record.title }} </h2>
    <h3 class="col-lg-12"> {{record.year}} </h3>
   
   </div>
  </div>

</template>

<script>
export default {
  name: 'Record',
  props:{
    record: Object
  }
}
</script>

<style lang="scss" scoped>

div.box{
  background-color: rgb(56, 56, 56);
  margin: 10px 10px;
  padding: 20px;
  transition: all 0.5s;
  &:hover{
    box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.329);
    cursor: pointer;
    transform: scale(1.15, 1.15);
    background: linear-gradient(-45deg, #968a8779, #c07e9765, #41697777, #63ffdb5b);
  }
  h2{
    font-size: 15px;
    color: white;
  }
  h3{
    font-size: 13px;
    color: gray;
  }
  img{
    height: 150px;
    width: 150px;
    margin-bottom: 10px;
  }
}

</style>