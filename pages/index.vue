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
            <p class="todoArea__text">▼ Add Task</p>
            <div class="todoArea__addtask todoArea__addtask--option">
              <div class="todoArea__input todoArea__input--option">
                <input
                  v-model="task"
                  type="text"
                  placeholder="Describe the task"
                />
                <span>{{ task }}</span>
              </div>
              <p class="todoArea__text">▼ Schedule</p>
              <div class="d-flex todoArea__box">
                <div class="todoArea__calendar">
                  <Datepicker />
                </div>
                <div class="todoArea__button">
                  <button id="addButton" class="button">追加</button>
                </div>
              </div>
            </div>
            <div class="todoArea__addList">
              <p class="todoArea__text">▼ Task List</p>
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
