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
    font-family:".SF NS Display";
  }
  h1{
    font-family: "Plantagenet Cherokee";
  }
  .main-content{
       margin: 4.5rem;

     }
  body{
    background-color: #FFF8F0 ;
  }
</style>
