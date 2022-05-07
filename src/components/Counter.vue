<template>
  <div>
    <div>
      <button v-on:click="decrement">decrement</button>
      <button v-on:click="increment">increment</button>
      <p>{{ count }}</p>

      <SubCounter @decrement="decrement"/>
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";
import SubCounter from "@/components/SubCounter.vue";

@Component({
  components: {
    SubCounter,
  },
})
export default class Counter extends Vue {
  protected count = 0;

  private decrement(): void {
    this.count += 1;
  }

  public increment(): void {
    if (this.count === 0) return;

    this.count -= 1;
  }
}
</script>

<style>
</style>