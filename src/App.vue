<template>
  <div id="app">
    <div id="nav">
      <h3>Learning TypeScript Tooling</h3>
      <Playground />
    </div>
  </div>
</template>
<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
import Playground from "./components/Playground.vue";

@Component({
  components: {
    Playground,
  },
})
export default class App extends Vue {}
</script>
<style>
</style>
