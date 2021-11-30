<template>
   <div class="searchcontainer">
       <input type="text" placeholder="Filtra Per Nome Dell'artista" v-model.trim="inputText">
       <button @click.prevent="$emit('search', inputText)">Search</button>
   </div>
</template>

<script>



export default {
  name: 'Search',
  data () {
      return {
          inputText: ""
      }
  }
}
</script>

<style lang="scss">
.searchcontainer {
    width: 100%;
    // display: flex;
    justify-content: center;
    // margin: 20px;
    text-align: center;
    // padding: 20px;
    padding-top: 20px;
    input {
        height: 30px;
        border: 3px solid black;
    }
    button{
        height: 30px;
        border: 3px solid black;
        font-weight: 1000;
    }
}

</style>
