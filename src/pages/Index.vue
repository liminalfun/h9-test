<template>
  <Layout>

    <Title/>

    <table>
      <tr>
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
  

    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Massa tincidunt dui ut ornare lectus sit. Aliquam sem et tortor consequat id porta nibh venenatis. At in tellus integer feugiat scelerisque varius morbi enim nunc. Eget est lorem ipsum dolor sit amet consectetur adipiscing. Diam sit amet nisl suscipit adipiscing bibendum est ultricies integer. Amet facilisis magna etiam tempor orci eu lobortis elementum nibh. Risus nec feugiat in fermentum posuere. Nulla facilisi cras fermentum odio eu feugiat. Quam nulla porttitor massa id neque aliquam vestibulum. Eros in cursus turpis massa tincidunt dui ut ornare. Nec tincidunt praesent semper feugiat nibh sed pulvinar. Semper auctor neque vitae tempus. Tincidunt vitae semper quis lectus nulla at volutpat. Auctor eu augue ut lectus arcu bibendum at varius.</p>

    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Massa tincidunt dui ut ornare lectus sit. Aliquam sem et tortor consequat id porta nibh venenatis. At in tellus integer feugiat scelerisque varius morbi enim nunc. Eget est lorem ipsum dolor sit amet consectetur adipiscing. Diam sit amet nisl suscipit adipiscing bibendum est ultricies integer. Amet facilisis magna etiam tempor orci eu lobortis elementum nibh. Risus nec feugiat in fermentum posuere. Nulla facilisi cras fermentum odio eu feugiat. Quam nulla porttitor massa id neque aliquam vestibulum. Eros in cursus turpis massa tincidunt dui ut ornare. Nec tincidunt praesent semper feugiat nibh sed pulvinar. Semper auctor neque vitae tempus. Tincidunt vitae semper quis lectus nulla at volutpat. Auctor eu augue ut lectus arcu bibendum at varius.</p>

    <button>Button</button>
    <!-- Learn how to use images here: https://gridsome.org/docs/images -->
    <g-image alt="Example image" src="~/favicon.png" width="135" />

  </Layout>
</template>

<script>
import Title from '~/components/Title.vue'
export default {
  metaInfo: {
    title: 'Hello, world!'
  },
  components: {
    Title
  }
}

</script>

<style>
.home-links a {
  margin-right: 1rem;
}

table {
  width: 60%;
  border-collapse: collapse;
}

tr {
  border: 1px black solid;
}

th {
    height: 16px;
    width: 32px;
}
td {
    height: 16px;
    width: 32px;
    border: 1px black solid;
}
</style>
