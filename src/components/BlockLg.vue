<template>
  <div class="block-lg">
    {{ message }}
  </div>
</template>

<script>
export default {
  name: 'BlockLg',
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
.block-lg {
  padding: 20px;
  background: #FFF;
}
</style>