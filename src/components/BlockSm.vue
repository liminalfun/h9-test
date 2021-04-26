<template>
  <div class="block-sm">
    {{ message }}
  </div>
</template>

<script>
export default {
  name: 'BlockSm',
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
.block-sm {
  padding: 20px;
  background: #FFF;
}
</style>