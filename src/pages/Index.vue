<template>
  <Layout>

    <section class="flex">

      <!-- Title -->
      <div class="title slide-in">
          <h1>Lorem Ipsum</h1>
      </div>

      <!-- Content -->
      <div class="block">
        <!-- Tables -->
        <div class="block-table block-lg">
          <div class="table-wrapper">
            <h2>ECC</h2>
            <Table/>
          </div>

          <div class="table-wrapper">
            <h2>Elementary School</h2>
            <Table/>
          </div>
        </div>

        <!-- Content with Buttons -->
        <div class="block-content block-sm">
          <div>
            <h2>Financial Aid</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Massa tincidunt dui ut ornare lectus sit. Aliquam sem et tortor consequat id porta nibh venenatis. At in tellus integer feugiat scelerisque varius morbi enim nunc. Eget est lorem ipsum dolor sit amet consectetur adipiscing. Diam sit amet nisl suscipit adipiscing bibendum est ultricies integer.</p>

            <a href="/" class="btn-primary">Button</a>
          </div>

          <div>
            <h2>Temple Beth Am Membership</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Massa tincidunt dui ut ornare lectus sit. Aliquam sem et tortor consequat id porta nibh venenatis. At in tellus integer feugiat scelerisque varius morbi enim nunc. Eget est lorem ipsum dolor sit amet consectetur adipiscing. Diam sit amet nisl suscipit adipiscing bibendum est ultricies integer.</p>

            <a href="/" class="btn-primary">Button</a>
          </div>
        
        </div>

      </div>


    </section>
  
  

    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Massa tincidunt dui ut ornare lectus sit. Aliquam sem et tortor consequat id porta nibh venenatis. At in tellus integer feugiat scelerisque varius morbi enim nunc. Eget est lorem ipsum dolor sit amet consectetur adipiscing. Diam sit amet nisl suscipit adipiscing bibendum est ultricies integer. Amet facilisis magna etiam tempor orci eu lobortis elementum nibh. Risus nec feugiat in fermentum posuere. Nulla facilisi cras fermentum odio eu feugiat. Quam nulla porttitor massa id neque aliquam vestibulum. Eros in cursus turpis massa tincidunt dui ut ornare. Nec tincidunt praesent semper feugiat nibh sed pulvinar. Semper auctor neque vitae tempus. Tincidunt vitae semper quis lectus nulla at volutpat. Auctor eu augue ut lectus arcu bibendum at varius.</p>

    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Massa tincidunt dui ut ornare lectus sit. Aliquam sem et tortor consequat id porta nibh venenatis. At in tellus integer feugiat scelerisque varius morbi enim nunc. Eget est lorem ipsum dolor sit amet consectetur adipiscing. Diam sit amet nisl suscipit adipiscing bibendum est ultricies integer. Amet facilisis magna etiam tempor orci eu lobortis elementum nibh. Risus nec feugiat in fermentum posuere. Nulla facilisi cras fermentum odio eu feugiat. Quam nulla porttitor massa id neque aliquam vestibulum. Eros in cursus turpis massa tincidunt dui ut ornare. Nec tincidunt praesent semper feugiat nibh sed pulvinar. Semper auctor neque vitae tempus. Tincidunt vitae semper quis lectus nulla at volutpat. Auctor eu augue ut lectus arcu bibendum at varius.</p>

    <button>Button</button>
    <!-- Learn how to use images here: https://gridsome.org/docs/images -->
    <g-image alt="Example image" src="~/favicon.png" width="135" />

  </Layout>
</template>

<script>
import Title from '~/components/Title.vue'
import Table from '~/components/Table.vue'
export default {
  setup() {
    const title = document.querySelector("Title");
    const blockSm = document.querySelector(".block-sm");
    let topOfBlockSm = blockSm.offsetTop;

    function handleTitle() {
      if (document.scrollY >= topOfBlockSm) {
        expandTitle;
        console.log('yes')
      } else {
        minimizeTitle;
        console.log('no')
      }
    }

    function expandTitle() {
      title.classList.add('block-lg');
    }

    function minimizeTitle() {
      title.classList.remove('block-lg');
    }

    onMounted(() => {
      slideInElements = Array.from(document.querySelectorAll('.slide-in'))
      document.addEventListener('scroll', handleTitle)
      handleScroll()
    })

    onUnmounted(() => {
      document.removeEventListener('scroll', handleTitle)
    })
  },
  methods: {
    // handleTitle() {
    //   if (window.scrollY >= topOfBlockSm) {
    //     expandTitle;
    //   } else {
    //     minimizeTitle;
    //   }
    // }
  },
  metaInfo: {
    title: 'Hello, world!'
  },
  components: {
    Title,
    Table
  }
}
</script>

<style lang="scss">


</style>
