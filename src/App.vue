<template>
  <div id="app">
    <div id="nav">
      <h3>Learning TypeScript Tooling</h3>
      <Playground :counter="appCounter" @counter-changed="counterChangeHandler" />
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
export default class App extends Vue {
  //  this will automatically become reactive data property
  appCounter = 0;

  counterChangeHandler(arg: string): void {
    switch (arg) {
      case "+":
        if (this.appCounter < 20) {
          ++this.appCounter;
        } else {
          alert("Max limit reached (20)");
        }
        break;
      case "-":
        if (this.appCounter !== 0) {
          --this.appCounter;
        } else {
          alert("Min limit reached (0)");
        }
        break;

      default:
        break;
    }
  }
}
</script>
<style>
</style>
