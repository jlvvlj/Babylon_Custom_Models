<template>
<div id="app">
  <BabylonExamples />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import BabylonExamples from './components/BabylonExamples.vue';

export default defineComponent({
  name: 'App',
  components: {
    BabylonExamples
  }
});
</script>

<style>
* {
  padding:0;
  margin:0; 
  background-size: cover;
  background-color: #33334d;
  background-position:center;
}

#app {
  width:100%;
  height:100%; 
  display:flex;
  justify-content: center;
  align-items: center; 
}



</style>
