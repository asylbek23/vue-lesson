<template>
  <div id="app">

    <ul>
      <li v-for="a in todos" :key="a.id" v-bind:class="{'eto-class':todos.completed}">{{a.title}}</li>
    </ul>

  </div>
</template>

<script>

export default {
  name: "App",
  data() {
    return {
      todos:[
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false
        },
        {
          "userId": 1,
          "id": 3,
          "title": "fugiat veniam minus",
          "completed": false
        },
        {
          "userId": 1,
          "id": 4,
          "title": "et porro tempora",
          "completed": true
        },
        {
          "userId": 1,
          "id": 5,
          "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
          "completed": false
        }
      ],
    }
  },
  methods: {
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
  font-size: 20px;
}

ul {
  margin: 0;
  padding: 0;
}

li {
  list-style: none;
}

.eto-class {
  color: red;
  font-size: 55px;
}

</style>
