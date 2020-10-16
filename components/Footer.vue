// footer

<template>
  <footer>
    <p>Copyright 2019 - {{ now }}</p>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      now: '',
    }
  },
  created() {
    const year = new Date()
    this.now = year.getFullYear()
  },
}
</script>
