<template>

  
  <div class="box col-lg-2 text-center text-uppercase">
    <img :src="record.poster" alt="">
    <h2> {{ record.title }} </h2>
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
  &:hover{
    box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.329);
    cursor: pointer;
    transform: scale(1.15, 1.15);
    background-color: rgba(128, 128, 128, 0.507);
    transition: width 2s, height 4s;
  }
  h2{
    font-size: 20px;
    color: white;
  }
  img{
    height: 150px;
    width: 150px;
    margin-bottom: 10px;
  }
}

</style>