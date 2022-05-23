<template>
  <div id="app">

    <!-- ADDITIONAL HOMEWORK -->
    <div class="color-change">
      <p class="item"><button v-on:click="changeColor">Change color</button></p>
    </div>

  </div>
</template>

<script>

export default {
  name: "AppChangeColor",
  data() {
    return {
      isColorChange: false,
    }
  },
  methods: {
    changeColor() {
      this.isColorChange = true;
    }
  }
};

</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
}

</style>