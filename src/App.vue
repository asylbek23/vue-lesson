<template>
  <div id="app">
    <div class="todo">
      <div class="todo__container">
        <!-- Title -->
        <div class="todo__title">My Todos</div>

        <!-- Header -->
        <div class="todo__header">
          <div class="todo__inputs">
            <div class="todo__input">
              <label for="">Name</label>
              <input type="text" class="todo__input-name">
            </div>
            <div class="todo__input">
              <label for="">Description</label>
              <input type="text" class="todo__input-descr">
            </div>
          </div>
          <button class="btn btn-add">Add Todo</button>
        </div>

        <!-- Content -->
        <div class="todo__content">
          <div class="todo__list list">
            <!-- List item 1 -->
            <div class="list__item">
              <div class="list__text">
                <div class="list__title">Task 1</div>
                <div class="list__descr">This is my task one</div>
              </div>
              <div class="list__btns">
                <button class="list__btn btn btn-complete">Complete</button>
                <button class="list__btn btn btn-delete">Delete</button>
              </div>
            </div>
            <!-- List item 2 -->
            <div class="list__item">
              <div class="list__text">
                <div class="list__title is-done">Task 2</div>
                <div class="list__descr is-done">This is my task two</div>
              </div>
              <div class="list__btns">
                <button class="list__btn btn btn-complete is-pressed">Complete</button>
                <button class="list__btn btn btn-delete">Delete</button>
              </div>
            </div>
            <!-- List item 3 -->
            <div class="list__item">
              <div class="list__text">
                <div class="list__title">Task 3</div>
                <div class="list__descr">This is my task three</div>
              </div>
              <div class="list__btns">
                <button class="list__btn btn btn-complete">Complete</button>
                <button class="list__btn btn btn-delete">Delete</button>
              </div>
            </div>
            <!-- List item 4 -->
            <div class="list__item">
              <div class="list__text">
                <div class="list__title">Task 4</div>
                <div class="list__descr">This is my task four</div>
              </div>
              <div class="list__btns">
                <button class="list__btn btn btn-complete">Complete</button>
                <button class="list__btn btn btn-delete">Delete</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
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
  color: #fff;
  margin-top: 60px;
  background-color: #333;
  padding: 40px;
  border-radius: 30px;

  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
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

</style>
