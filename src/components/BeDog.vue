<template>
    <be-media v-bind:src="src" @click.native="refresh()"/>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import BeMedia from './BeMedia.vue';
import Axios from 'axios';

@Component({
components: {
  BeMedia,
},
})

export default class BeDog extends BeMedia {

  constructor() {
    super();
    this.refresh();
  }

  public refresh() {
    Axios.get('https://random.dog/woof.json')
      .then((response) => this.src = response.data.url)
      .catch((error) => console.error(error));
  }
}
</script>

<style>
</style>