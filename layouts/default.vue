<template>
  <div>
    <TheHeader></TheHeader>
    <main class="main-content">
      <nuxt/>
    </main>

  </div>
</template>
<script>
  import TheHeader from '@/components/TheHeader/TheHeader'

  export default {
    components:{
      TheHeader: TheHeader
    }
  }
</script>
<style>
  *{
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
  }
  p{
    font-family:".SF NS Display", sans-serif;
  }
  h1{
    font-family: "Plantagenet Cherokee", sans-serif;
  }
  .main-content{
       margin: 4.5rem;

     }
</style>
