<template>
  
  <div>
    <Nav/>
    <div class="layout">
      <slot/>
    </div>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
  import Nav from '~/components/Nav.vue'

  export default {
    components: {
      Nav
    }
  }
</script>

<style>
body {
  margin:0;
  padding:0;
  line-height: 1.5;
}

.layout {
  max-width: 100vw;
  margin: 0 auto;
}
</style>
