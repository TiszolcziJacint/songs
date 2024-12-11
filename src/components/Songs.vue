<template>
  <div>
    <table class="table">
      <thead>
        <tr>
          <th>Title</th>
          <th>Year</th>
          <th>BPM</th>
          <th>Time</th>
          <th>Genre</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="song in props.songs" v-bind:key="song" v-bind:song="song">
          <td>{{ song.TITLE }}</td>
          <td>{{ song.YEAR }}</td>
          <td>{{ song.BPM  }}</td>
          <td>{{ song.TIME }}</td>
          <td>{{ song.GENRE }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>

  const props = defineProps(['songs']);

</script>

<style scoped>

</style>
