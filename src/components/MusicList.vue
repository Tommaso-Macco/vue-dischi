<template>
    <main>
        <div>
            <Search @search="searching" />
        </div>
        <div class="music-container">
            <MusicNow
                v-for="music, i in filterdMusic"
                :key="i"
                :details="music"
            />
        </div>
    </main>
</template>

<script>
import MusicNow from '../components/MusicNow.vue';
import Search from '../components/Search.vue';
import axios from 'axios';



export default {
  name: 'MusicList',
  components: {
      MusicNow,
      Search
  },
  data () {
      return {
          apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
          allMusic: [],
          searchText: "",
      }
  },
  created () {
      this.getMusic();
  },

   computed: {
       filterdMusic() {
           if (this.searchText === "") {
               return this.allMusic;
           }
            return this.allMusic.filter((item) => {
                return item.author.toLowerCase().includes(this.searchText.toLowerCase());
            })
       }
   },
  methods: {
      getMusic () {
          axios
          .get(this.apiUrl)
          .then((result) => {
              this.allMusic = result.data.response;
            //   console.log(result.data.response);
          })
      },
      searching(text) {
          this.searchText = text;
          console.log(this.searchText);
      }
  }
}
</script>

<style lang="scss">
    main {
        height: calc(100vh - 80px);
        background-color: #1e2d3b;

        .music-container {
            width: 70%;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }
    }
</style>
