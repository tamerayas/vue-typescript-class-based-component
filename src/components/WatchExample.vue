<template>
  <div>WatchExample</div>
</template>

<script lang="ts">
import { Component, Prop, Vue, Watch } from "vue-property-decorator";
import Counter from "./Counter.vue";

@Component({
  components: {
    Counter,
  },
})
export default class WatchExample extends Vue {
  //Prop
  @Prop()
  protected val: number;

  @Watch('val')
  onValChanged(val: number) {
    console.log(val);
  }





  

  //Watch Example
  
}
</script>

<style>
</style>