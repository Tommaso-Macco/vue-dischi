<template>
    <div class="musicbox">
        <img :src="details.poster" :alt="details.title">
        <h3> {{details.title.toUpperCase()}} </h3>
        <div> {{details.author}} </div>
        <div> {{details.year}} </div>
    </div>
</template>

<script>


export default {
  name: 'MusicNow',
  props: {
      details: Object,
  }

}
</script>

<style lang="scss">
    .musicbox {
        width: calc(20% - 40px);
        background-color: #2e3a46;
        padding: 20px;
        margin-left: 20px;
        margin-right: 20px;
        margin-top: 40px;
        cursor: pointer;
        img {
            max-width: 95%;
        }
        h3 {
            text-align: center;
            color: #fff;
            padding-top: 15px;
            padding-bottom: 15px;
        }
        div {
            text-align: center;
            color: grey;
        }
    }
</style>
