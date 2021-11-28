<template>
    <div class="musicbox">
        <!-- <img :src="details.poster" :alt="details.title"> -->
        <!-- <h3> {{details.title.toUpperCase()}} </h3> -->
        <div> {{details.author}} </div>
        <!-- <div> {{details.year}} </div> -->
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
        width: calc(100% / 5);
        img {
            max-width: 100%;
        }
    }
</style>
