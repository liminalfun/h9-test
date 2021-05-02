<template>
  <div class="nav">
    <a href="/">{{ message }}</a>
    <a class="btn" href="/">
      <span>{{ buttonText }}</span>
    </a>
  </div>
</template>

<script>
export default {
  name: 'Nav',
  data () {
    return {
      message: 'Sitename',
      buttonText: 'Back'
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

.btn {
  position: fixed;
  top: 0.4rem;
  right: 1.4rem;
  height: 2.75rem;
  width: 2.75rem;
  border-radius: 100px;
  background-color: $black;
  border: none;
  display: flex;
  transition: all .5s;
  span {
    display: hidden;
    opacity: 0;
    color: $white;
    text-align: center;
    font-weight: 400;
    font-size: 40px;
    margin: 0 auto;
    align-self: center;
    transition: all .5s;
  }
  @include md {
    height: 5.5rem;
    min-width: 5.5rem;
    top: 1.4rem;
    right: 1.3rem;
  }
  @include lg {
    top: 6.25rem;
    right: 1.3rem;
    &:hover {
      padding: 0 1rem;
      span {
        display: inline-block;
        opacity: 100%;

      }
    }
  }
}
</style>