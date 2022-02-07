<template>
  <div>
    <button @click="increment">increment</button>
    <button @click="decrement">decrement</button>
    <p>{{ morality }}</p>
  </div>
</template>
<script>
export default {
  name: "App",
  data() {
    return { morality: 0 };
  },
  methods: {
    increment() {
      this.morality++;
    },
    decrement() {
      this.morality--;
    },
  },
};
</script>