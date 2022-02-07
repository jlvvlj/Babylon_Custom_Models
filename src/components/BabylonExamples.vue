<template>
<div>
<h3>Emergent Engine Showcase - Synchronicity</h3>
<p>Morality:{{morality}} Purity:{{purity}}</p>
<div class="wrapper">
  <button @click="decrementMorality" class="button-74">Kill NPC</button>
  <button @click="incrementMorality" class="button-74">Help Villagers</button>
</div>
<canvas></canvas>
</div>

</template>

<script lang="ts">
import { defineComponent } from 'vue';
import {CustomModels} from "@/BabylonExamples/CustomModels"



export default defineComponent({
  name: 'BabylonExamples',
  mounted(){
    const canvas = document.querySelector("canvas")!;
    new CustomModels(canvas);
  },
  data() {
    return { morality: 120, purity: 80 };
  },
  methods: {
    incrementMorality() {
      this.morality++;
    },
    decrementMorality() {
      this.morality--;
    },
    incrementPurity() {
      this.purity++;
    },
    decrementPurity() {
      this.purity--;
    },
  },
  
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto+Condensed&family=Roboto:wght@100;700&display=swap');

div {
  width:150%;
  height:150%;
  display:flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background:none;
}
h3 {
  font-family: 'Roboto Condensed', sans-serif;
  font-size: 2em;
  color: #fff;
  text-align: center;
  margin: 15px;
}
p {
  color:white;
  background:none;
  margin-bottom:1rem;
 font-family: 'Roboto Condensed';
  font-weight: 300;
  font-size:1.5rem;
  margin: 15px;
}

canvas {
  width:100%;
  height:100%;
  border:none;
  outline:none;
  box-shadow:8px 8px 10px -6px #000000;
}


.wrapper {
    display: flex;
    grid-gap: 10px;
  }

  .box {
    background-color: #444;
    color: #fff;
    border-radius: 5px;
    padding: 20px;
    font-size: 150%;

  }

  
.button-74 {
  background-color: #fbeee0;
  border: 2px solid #422800;
  border-radius: 30px;
  box-shadow: #422800 4px 4px 0 0;
  color: #422800;
  cursor: pointer;
  display: inline-block;
  font-weight: 600;
  font-size: 18px;
  padding: 0 18px;
  line-height: 50px;
  text-align: center;
  text-decoration: none;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

.button-74:hover {
  background-color: #fff;
}

.button-74:active {
  box-shadow: #422800 2px 2px 0 0;
  transform: translate(2px, 2px);
}

@media (min-width: 768px) {
  .button-74 {
    min-width: 120px;
    padding: 0 25px;
  }
}

</style>
