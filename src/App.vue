<template>
  <div id="app">

    <!-- ADDITIONAL HOMEWORK -->
    <div class="additional">
      <p v-for="a in tasks" :key="a.id">
        {{a.id}} {{a.title}}
        <button v-on:click="deleteItem(a)">Delete</button>
      </p>
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
      ],
    }
  },
  methods: {
    deleteItem(task) {
      // console.log('deleted');
      // console.log(this.tasks);
      console.log(task);
      task.title = 'Title changed'
    },
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
