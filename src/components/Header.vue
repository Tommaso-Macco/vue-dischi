<template>
   <header>
       <div id="logo-cont">
           <img src="../img/spotify.png" alt="">
       </div>
   </header>
</template>

<script>



export default {
  name: 'Header',
}
</script>

<style lang="scss">
    #logo-cont {
        height: 100px;
        display: flex;
        align-items: center;
        background-color: #2e3a46;
        img {
            height: 100%;
            padding-left: 20px;
            padding-top: 17px;
            padding-bottom: 17px;
        }
    }
</style>
