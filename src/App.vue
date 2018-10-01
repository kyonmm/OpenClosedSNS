<template>
  <div id="app">
    <Thread
      :threadStart="'hoge'"
      :comments="['piyo', 'fuga']"
    />
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';
import Thread from './components/Thread.vue';

@Component({
  components: {
    Thread
  },
})
export default class App extends Vue {
  comments: string[] = ["piyo", "foo"];
}
</script>

<style>

</style>
