<template>
  <div>
    <h3>Welcome to counter game!</h3>
    <hr />
    <h4>Counter: {{counter}}</h4>
    <button @click="clickHandler('+')">Increment</button>
    <br />
    <button @click="clickHandler('-')">Decrement</button>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
import { Prop } from "vue-property-decorator";

@Component
export default class Playground extends Vue {
  //  Declaring a prop
  @Prop() counter!: number;

  clickHandler(arg: string): void {
    console.log("Handler called", arg);
  }
}
</script>

<style>
</style>