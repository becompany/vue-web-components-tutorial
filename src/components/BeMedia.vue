<template>
  <img v-if="isImage()" v-bind:src="src"/>
  <video v-else autoplay> <source v-bind:src="src" type="video/mp4"> </video>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class BeMedia extends Vue {
  @Prop() protected src!: string;
  private isImage() {
    return this.src.endsWith('mp4') ? false : true;
  }
}
</script>

<style>
</style>
