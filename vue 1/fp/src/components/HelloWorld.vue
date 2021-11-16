<template>
  <div class="hello">
    {{ message }}
    <br />
    <input type="number" placeholder="operand1" v-model.number="operand1" />
    <input type="number" placeholder="operand2" v-model.number="operand2" />
    <br />
    {{ result }}
    <br />
    <button v-on:click="result = operand1 + operand2">+</button>
    <button v-on:click="result = operand1 - operand2">-</button>
    <button @click="result = operand1 * operand2">*</button>
    <button @click="result = operand1 / operand2">/</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      message: "HelloVue",
      result: 0,
      operand1: 0,
      operand2: 0,
    };
  },
  methods: {
    add() {
      this.result = this.operand1 + this.operand2;
    },
    substract() {
      this.result = this.operand1 - this.operand2;
    },
    divide() {
      this.result = this.operand1 / this.operand2;
    },
    muliply() {
      this.result = this.operand1 * this.operand2;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
