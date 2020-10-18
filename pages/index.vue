<template>
  <div class="container">
    <Header />
    <div class="kv">
      <div class="kv__inner d-flex justify-content-center align-items-center">
        <h2 class="title title--option">todoVue</h2>
      </div>
    </div>
    <div class="wrap">
      <!-- Todo App -->
      <section class="secTodo">
        <div class="todo inner">
          <h2 class="todo__title">ToDo Lists</h2>
          <div class="todoArea">
            <h3 class="todoArea__title">Add Task</h3>
            <div class="todoArea__addtask todoArea__addtask--option">
              <div class="d-flex">
                <p class="todoArea__input todoArea__input--option">
                  <input
                    v-model="task"
                    type="text"
                    placeholder="Describe the task"
                  />
                  <span>{{ task }}</span>
                </p>
                <p class="todoArea__calendar">
                  <Datepicker />
                  <!-- <input type="text" /> -->
                </p>
              </div>
              <p class="todoArea__button">
                <button id="addButton" class="button">追加</button>
              </p>
            </div>
            <div class="todoArea__addList">
              <h3 class="todoArea__title">Task List</h3>
              <ul class="todoArea__list todoArea__list--option">
                <li
                  class="listItem d-flex justify-content-between align-items-center"
                >
                  <p>
                    テスト<span class="period period--option"
                      >期間：2020-10-19</span
                    >
                  </p>
                  <span class="delete">×</span>
                </li>
                <li
                  class="listItem d-flex justify-content-between align-items-center"
                >
                  <p>
                    テスト<span class="period period--option"
                      >期間：2020-10-19</span
                    >
                  </p>
                  <span class="delete">×</span>
                </li>
                <li
                  class="listItem d-flex justify-content-between align-items-center"
                >
                  <p>
                    テスト<span class="period period--option"
                      >期間：2020-10-19</span
                    >
                  </p>
                  <span class="delete">×</span>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </section>
      <!-- Todo App END -->
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  data() {
    return {
      task: '',
    }
  },
}
</script>
