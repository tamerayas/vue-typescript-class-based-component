<template>
  <div id="app">
    <Counter @changed="changed" />
    <WatchExample :val="changedVal" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Counter from "@/components/Counter.vue"
import WatchExample from "@/components/WatchExample.vue"

@Component({
  components: {
    Counter,
    WatchExample
  },
})
export default class App extends Vue {
  public changedVal = 0;

  private changed(val: number):void {
    console.log('counterVal', val);
    this.changedVal = val
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
