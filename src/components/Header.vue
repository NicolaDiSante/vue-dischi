<template>
  <header>
    <div class="image">
      <img src="@/assets/img/logo-small.svg" alt="">
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss" scoped>

header{
  height: 60px;
  width: 100%;
  background-color: rgb(75, 75, 75);
  .image{
    padding: 10px;
    img{
    height: 40px;
    width: 40px;
    color: green;
    cursor: pointer;
  }
  }
  
}


</style>