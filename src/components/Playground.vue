<template>
  <div>
    <h3>Welcome to counter game!</h3>
    <hr />
    <h4>Counter: {{counter}}</h4>
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
}
</script>

<style>
</style>