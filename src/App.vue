<template>
  <div id="app" class="container">
    <div class="row">
      <div class="col-6">
        <be-dog class="img-fluid"/>
      </div>
      <div class="col-6">
        <be-cat class="img-fluid"/>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import BeDog from './components/BeDog.vue';
import BeCat from './components/BeCat.vue';
import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap-vue/dist/bootstrap-vue.css';

@Component({
  components: {
    BeDog,
    BeCat,
  },
})
export default class App extends Vue {}
</script>

<style>
</style>
