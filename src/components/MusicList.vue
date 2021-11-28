<template>
    <main>
        <div class="music-container">

        </div>

        <MusicNow
            v-for="music, i in allMusic"
            :key="i"
            :details="MusicNow"
        />
    </main>
</template>

<script>
import MusicNow from '../components/MusicNow.vue'
import axios from 'axios'



export default {
  name: 'MusicList',
  components: {
      MusicNow
  },
  data () {
      return {
          apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
          allMusic: [],
      }
  },
  created () {
      this.getMusic();
  },
  methods: {
      getMusic () {
          axios
          .get(this.apiUrl)
          .then((result) => {
              this.allMusic = result.data.response;
              console.log(result.data.response);
          })
      }
  }
}
</script>

<style lang="scss">
    main {
        height: calc(100vh - 100px);
        background-color: #1e2d3b;

        .music-container {
            height: 100%;
            width: 60%;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            flex: wrap;
        }
    }
</style>
