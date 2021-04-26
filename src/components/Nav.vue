<template>
  <div class="nav">
    <a href="/">{{ message }}</a>
  </div>
</template>

<script>
export default {
  name: 'Nav',
  data () {
    return {
      message: 'Site Title'
    }
  },
  methods: {
  }
}
</script>

<style>
.nav {
  padding: 20px;
  background: #FFF;
}
</style>