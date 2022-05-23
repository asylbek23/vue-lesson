<template>
  <div id="app">

    <!-- ADDITIONAL HOMEWORK -->
    <div class="additional">
      <p v-for="task in tasks" :key="task.id"><button v-on:click="deleteItem(task)">Delete</button></p>
    </div>

  </div>
</template>

<script>

export default {
  name: "App",
  data() {
    return {
      tasks:[
        {id:1, title:'baga'},
        {id:2, title:'Mars'},
        {id:3, title:'Germany'}
      ]
    }
  },
  methods: {
    deleteItem(e) {
      console.log(e);
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
