<template>
  <h1>Calculate Grade</h1>
  <input v-model="num1" type="number" title="grade 1" @input="sumNumbers"/> 
  <input v-model="num2" type="number" title="grade 2" @input="sumNumbers"/> 
  <h1>Grade: {{ sum }}</h1>

  <h1 v-if="sum > 75">Passed</h1>
  <h1 v-else>Failed</h1>

  <ul v-for="number in numbers">
    <li>{{ number }}</li>
  </ul>
  
</template>

<script>
export default {
  name: "kevinApp",
  data() { 
    return {
      num1: 0,
      num2: 0,
      sum: 0,
      numbers: [1, 2, 3, 4, 5]
    };
  },
  methods: {
    sumNumbers() {
      this.sum = this.num1 + this.num2;
    },
  }
}
</script>