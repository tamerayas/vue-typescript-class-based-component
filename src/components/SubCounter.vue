<template>
  <button @click="addToCount">SubCounterrrr</button>
</template>

<script lang="ts">
import { Component, Vue, Emit } from "vue-property-decorator";

@Component
export default class SubCounter extends Vue {
  // Both of decrement emit and addToCount method works.
  @Emit("decrement")
  addToCount() {
    return;
  }

  /* 
  Or
  // It just runs emit ( this.$emit('decrement') )
  @Emit("decrement")
  addToCount() {
    return;
  }
  */

  private mounted() {
    console.log("mounted");
  }
}
</script>

<style>
</style>