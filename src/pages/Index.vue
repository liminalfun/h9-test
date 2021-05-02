<template>
  <Layout>

    <Title/>

    <section class="content">
      
      <!-- Tables -->
      <div class="block-lg">
        <div class="table-wrapper block-lg">
          <h2>ECC</h2>
          <Table/>
        </div>
        
        <div class="table-wrapper">
          <h2>Elementary School</h2>
          <Table/>
        </div>
      </div>

      <!-- Content with Buttons -->
      <div class="block-sm" v-scroll="expandSm">
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

      <div class="block-full">
        <img src="https://images.unsplash.com/photo-1516331138075-f3adc1e149cd?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1983&q=80" alt="nebula in galaxy"/>
      </div>

      <div class="block-md" v-scroll="expandMd">
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

      <div class="block-lg">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Massa tincidunt dui ut ornare lectus sit. Aliquam sem et tortor consequat id porta nibh venenatis. At in tellus integer feugiat scelerisque varius morbi enim nunc. Eget est lorem ipsum dolor sit amet consectetur adipiscing. Diam sit amet nisl suscipit adipiscing bibendum est ultricies integer. Amet facilisis magna etiam tempor orci eu lobortis elementum nibh. Risus nec feugiat in fermentum posuere. Nulla facilisi cras fermentum odio eu feugiat. Quam nulla porttitor massa id neque aliquam vestibulum. Eros in cursus turpis massa tincidunt dui ut ornare. Nec tincidunt praesent semper feugiat nibh sed pulvinar. Semper auctor neque vitae tempus. Tincidunt vitae semper quis lectus nulla at volutpat. Auctor eu augue ut lectus arcu bibendum at varius.</p>
      </div>
    </section>

  </Layout>
</template>

<script>
import Title from '~/components/Title.vue'
import Table from '~/components/Table.vue'
export default {
  directives: {
    scroll: {
      inserted: function (el, binding) {
        let f = function (evt) {
          if (binding.value(evt, el)) {
            window.removeEventListener('scroll', f)
          }
        }
        window.addEventListener('scroll', f)
      }
    }
  },
methods: {
    expandSm: function (evt, el) {
      const smBlocks = document.querySelectorAll(".block-sm");
      const title = document.querySelector(".title");
      smBlocks.forEach(smBlock => {
        let slideInAt = (window.scrollY + window.innerHeight) - smBlock.offsetHeight / 6;
        let isHalfShown = slideInAt > smBlock.offsetTop;
        let smBottom = smBlock.offsetTop + smBlock.offsetHeight / 2 ;
        let isNotScrolledPast = window.scrollY < smBottom;

        if (isHalfShown && isNotScrolledPast ) {
          title.classList.add('title-lg');
          console.log('smBottom ' + smBlock.offsetHeight)
          console.log('scrollY ' + window.scrollY)
        } else {
          title.classList.remove('title-lg')
        }
      })
    },
    expandMd: function (evt, el) {
      const mdBlocks = document.querySelectorAll(".block-md");
      const title = document.querySelector(".title");
      mdBlocks.forEach(mdBlock => {
        let slideInAt = (window.scrollY + window.innerHeight) - mdBlock.offsetHeight / 6;
        let isHalfShown = slideInAt > mdBlock.offsetTop;
        const mdBottom = mdBlock.offsetTop + mdBlock.offsetHeight / 2;
        const isNotScrolledPast = window.scrollY < mdBottom;

        if (isHalfShown && isNotScrolledPast) {
          title.classList.add('title-md')
        } else {
          title.classList.remove('title-md')
        }
      })
    }
  },
  metaInfo: {
    title: 'Home'
  },
  components: {
    Title,
    Table
  }
}
</script>

<style lang="scss">


</style>
