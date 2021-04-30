<template>
  <div class="nav">
    <a href="/">{{ message }}</a>
    <button href="/"></button>
  </div>
</template>

<script>
export default {
  name: 'Nav',
  data () {
    return {
      message: 'Sitename'
    }
  },
  methods: {
  }
}
</script>

<style lang="scss" scoped>

.nav {
  padding: 0.5rem 1rem 1.4rem;
  position: sticky;
  top: 0;
  left: 0;
  background-color: $blue;
  z-index: 1;
  @include md {
    padding: 1.6rem 1.9rem 2rem;
  }
  @include lg {
    background: $white;
    padding: 12px 30px;
  }

  a {
    font-size: 18px;
    text-decoration: none;
    color: inherit;
    font-weight: normal;
    @include md {
      font-size: 30px;
    }
  }
}

button {
  position: fixed;
  top: 0.4rem;
  right: 1.4rem;
  height: 2.75rem;
  width: 2.75rem;
  border-radius: 100%;
  background-color: $black;
  border: none;
  @include md {
    height: 5.5rem;
    width: 5.5rem;
    top: 1.4rem;
    right: 1.3rem;
  }
  @include lg {
    top: 6.25rem;
    right: 1.3rem;
  }
}
</style>