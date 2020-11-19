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
            <Addtask />
            <Tasklist />
          </div>
        </div>
      </section>
      <!-- Todo App END -->
    </div>
    <Footer />
  </div>
</template>

<script>
import Tasklist from '@components/Tasklist.vue'
import Addtask from '@components/Addtask.vue'

export default {
  components: { Tasklist, Addtask },
}
</script>
