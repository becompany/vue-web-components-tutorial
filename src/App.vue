<template>
  <div id="app">
    <be-media src="https://random.dog/29c13d4e-9bec-45db-98b4-5b8df0f4dd95.png"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import BeMedia from './components/BeMedia.vue';

@Component({
  components: {
    BeMedia,
  },
})
export default class App extends Vue {}
</script>

<style>
</style>
