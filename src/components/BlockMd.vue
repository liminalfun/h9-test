<template>
  <div class="block-md">
    {{ message }}
  </div>
</template>

<script>
export default {
  name: 'BlockMd',
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
.block-md {
  padding: 20px;
  background: #FFF;
}
</style>