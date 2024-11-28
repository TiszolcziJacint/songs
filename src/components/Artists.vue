<template>
  <div>
    <select class="form-select" @change="getArtist($event)">
      <option disabled  selected>Select an artist</option>
      <option v-for="artist in props.artists" :value="artist._id">{{artist.artist}}</option>
    </select>
  </div>
</template>

<script setup>

  const props = defineProps(['artists']);
  const emits = defineEmits(['getArtist']);

  const getArtist = event => {
    const id = event.target.value;
    emits('getArtist', id);
  }

</script>

<style scoped>

</style>
