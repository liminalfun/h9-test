<template>
  <div class="title">
    {{ message }}
  </div>
</template>

<script>
export default {
  name: 'Title',
  data () {
    return {
      message: 'Lorem Ipsum'
    }
  },
  methods: {
  }
}
</script>

<style>
.title {
  padding: 20px;
  background: #FFF;
}
</style>