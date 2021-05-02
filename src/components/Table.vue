<template>
  <table>
    <tr>
      <th></th>
      <th></th>
      <th></th>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </table>
</template>

<script>
export default {
  name: 'Table',
}
</script>

<style lang="scss">

  table {
    margin-top: 0.4rem;
    width: 100%;
    border-collapse: collapse;
    table-layout: fixed;
  }

  td, th {
    border: 1px $black solid;
    height: 1.9rem;
    @include md {
      height: 3.25rem;
    }
  }

  td:first-child, th:first-child {
    border-left: none;
  }

  td:last-child, th:last-child {
    border-right: none;
  }
</style>