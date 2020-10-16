// header

<template>
  <header>
    <h1>Yu Ecchuya Site</h1>
    <nav class="nav">
      <Nav />
    </nav>
    <!-- sp Navigation -->
    <nav class="nav nav--sp">
      <span class="swiciNav swiciNav--option" @click="isActive = !isActive">
        ▼ MENU
      </span>
      <div :class="{ active: isActive }" class="navArea">
        <Nav />
      </div>
    </nav>
    <!-- sp Navigation -->
  </header>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
    }
  },
}
</script>
