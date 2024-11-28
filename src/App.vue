<template>
  <div class="container">
    <Artists :artists="artistData" @getArtist="getSongsById($event)"/>
    <Songs v-if="songs.length" :songs="songs"/>
  </div>
</template>

<script setup>
  import { ref } from 'vue';
  import artistData from './assets/artists.js';
  import songsData from './assets/songs.js';
  import Artists from './components/Artists.vue';
  import Songs from './components/Songs.vue';

  const songs =  ref([]);

  const getSongsById = (songId) => {
    songs.value = songsData.filter(song => song.ARTIST_ID == songId);
  }
</script>
<style scoped>

</style>
