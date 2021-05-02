<template>
  <div class="title">
    <h1>{{ message }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Title',
  data () {
    return {
      message: 'Lorem Ipsum'
    }
  }
}
</script>

<style lang = "scss">
  .title {
    padding: 0.5rem 1.5rem;
    @include md {
      padding: 1.5rem 2.8rem;
    }
    @include lg {
      position: fixed;
      height: calc(100vh - 4.3rem);
      background-color: $blue;
      padding: 3.4rem 7rem 3.5rem 3rem;
      width: calc(40vw - 10rem);
      top: 4.3rem;
      transition: all .5s;
    }
  }
  
  .title-lg {
    @include lg {
      width: calc(60vw - 10rem);
    }
  }

  .title-md {
    @include lg {
      width: calc(50vw - 10rem);
    }
  }

</style>