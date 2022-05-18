<template>
  <div id="app">

    <!-- TODO -->
    <div class="todo">
      <div class="todo__container">
        <!-- Title -->
        <div class="todo__title">My Todos</div>

        <!-- Header -->
        <div class="todo__header">
          <div class="todo__inputs">
            <div class="todo__input">
              <label for="">Name</label>
              <input type="text" class="todo__input-name" v-bind:value="name" v-on:input="setName">
            </div>

            <div class="todo__input">
              <label for="">Description</label>
              <input type="text" class="todo__input-descr" v-bind:value="description" v-on:input="setDescription">
            </div>

          </div>
          <button class="btn btn-add" v-on:click="addTodo">Add Todo</button>
        </div>

        <!-- Content -->
        <div class="todo__content">
          <div class="todo__list list">

            <!-- List item 1 -->
            <div class="list__item" v-for="a in todos" :key="a.name">
              <div class="list__text">
                <div class="list__title" >{{a.name}}</div>
                <div class="list__descr" >{{a.description}}</div>
              </div>
              <div class="list__btns">
                <button class="list__btn btn btn-complete" v-on:click="taskComplete">Complete</button>
                <button class="list__btn btn btn-delete" v-on:click="deleteTaskItem">Delete</button>
              </div>
            </div>

          </div>
        </div>
      </div>
    </div>


    <!-- ADDITIONAL HOMEWORK -->
    <div class="additional">
      <p>Additional</p>
    </div>

  </div>
</template>

<script>
export default {
  name: "App Todo",
  data() {
    return {
      name: "",
      description: "",
      todos: [],
      deleteTask: true
    }
  },
  methods: {
    setName(e) {
      this.name = e.target.value;
      console.log(e.target.value);
    },

    setDescription(e) {
      this.description = e.target.value;
      console.log(e.target.value);
    },

    addTodo() {
      let todo = {
        name: this.name,
        description: this.description,
        done: false
      }

      this.todos.push(todo);
    },

    taskComplete() {
      let findDone = this.todos.find(item => item.done === false);

      let todoDoneState = findDone.done;

      const listTitle = document.querySelector('.list__title');
      const listDescription = document.querySelector('.list__descr');
      const btnComplete = document.querySelector('.btn-complete');

      if (todoDoneState == false) {
        listTitle.classList.add('is-done');
        listDescription.classList.add('is-done');
        btnComplete.classList.add('is-pressed');
      } else {
        listTitle.classList.remove('is-done');
        listDescription.classList.remove('is-done');
        btnComplete.classList.remove('is-pressed');
      }

      // console.log(findDone.done);
    },

    deleteTaskItem() {
      let blabla = this.deleteTask;
      blabla = false;
      console.log(blabla);
    }

  }
};
</script>

<style>

body {
  background-color: #dbdbdb;
  /* font-size: 20px; */
}

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

.title {
  font-size: 26px;
  font-weight: 600;
}

.todo {
  color: #fff;
  background-color: #333;
  padding: 40px;border-radius: 30px;
}

.todo__container {
  max-width: 700px;
  margin: 0 auto;
}

.todo__header,
.todo__content {
  border-radius: 5px;
  background-color: #444;
}

.todo__title {
  font-size: 26px;
  font-weight: 600;
}

.todo__header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  margin-top: 20px;
}

.todo__inputs {
  display: flex;
}

.todo__input {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-right: 10px;
}

.todo__input input {
  border-radius: 10px;
  outline-color: orange;
  background-color: #fff;
  border-color: orange;
  margin-top: 5px;
  padding: 5px 10px;
}

.todo__content {
  margin-top: 20px;
}

button {
  border: none;
  cursor: pointer;
  border-radius: 30px;
  display: inline-block;
  font-size: 14px;
  padding: 7px 14px;
  font-weight: 600;
}

.btn-add {
  background-color: #f90;
  color: #fff;
}

.list__item {
  border-bottom: 1px solid #333;
  padding: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.list__text {
}

.list__title {
  color: #f90;
  font-weight: 600;
  font-size: 26px;
  text-align: left;
}

.list__descr {
  font-size: 14px;
  margin-top: 5px;
}

.btn-complete,
.btn-delete {
  background-color: #fff;
}

.btn-complete {
  color: rgb(0, 185, 145);
  border: 1px solid rgb(0, 185, 145);
  margin-right: 15px;
}

.btn-delete {
  color: rgb(185, 0, 0);
  border: 1px solid rgb(185, 0, 0);
  margin-right: 15px;
}

.btn-complete.is-pressed {
  display: none;
}

.list__title.is-done,
.list__descr.is-done {
  color: #777;
  text-decoration: line-through;
}

.is-disable {
  display: none;
}

</style>
