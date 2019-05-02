<template>
  <section class="container flex-col justify-start bg-white">
    <nav-in-page active="priceRange"/>
    <div class="w-full inline-flex flex-row justify-start my-4">
      <no-ssr>
        <vue-slider
          ref="priceRange"
          class="w-full md:w-1/2 mx-4 my-2"
          v-model="value"
          :interval="interval"
          tooltip="none"
          :max="maxPrice"
          :adsorb="true"
          :marks="marks"
          :contained="true"
        ></vue-slider>
      </no-ssr>
      <div class="inline-block relative w-full md:w-48">
        <select
          class="block appearance-none w-full bg-white border border-grey-light hover:border-grey px-4 py-2 pr-8 rounded shadow leading-tight focus:outline-none focus:shadow-outline"
        >
          <option>Most Popular</option>
          <option>Newest</option>
          <option>Lowest to Highest</option>
          <option>Highest to Lowest</option>
        </select>
        <div
          class="pointer-events-none absolute pin-y pin-r flex items-center px-2 text-grey-darker"
        >
          <svg class="fill-current h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
            <path d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"></path>
          </svg>
        </div>
      </div>
    </div>
    <div class="flex flex-row flex-wrap w-full justify-start">
      <!-- recommend list -->
      <product-card
        class="w-1/3 p-4"
        url
        af-url
        img-url="https://tailwindcss.com/img/card-top.jpg"
        title="The Coldest Sunset"
        desc="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil."
      />
      <product-card
        class="w-1/3 p-4"
        url
        af-url
        img-url="https://tailwindcss.com/img/card-top.jpg"
        title="The Coldest Sunset"
        desc="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil."
      />
    </div>
  </section>
</template>

<script>
import NavInPage from '~/components/NavInPage.vue'
import ProductCard from '~/components/ProductCard.vue'

export default {
  data() {
    return {
      value: [0, 100],
      maxPrice: 1100,
      interval: 100,
      position: ['bottom', 'bottom'],
      marks: val =>
        val > 1000
          ? {
              label: `MAX`,
              labelActiveStyle: {
                color: '#3498db'
              }
            }
          : val % 100 === 0
          ? {
              label: `${val}元`,
              labelActiveStyle: {
                color: '#3498db'
              }
            }
          : false
    }
  },
  mounted() {
    console.log(this.$route.query.to)
  },
  updated() {
    if (this.$refs.priceRange.$el.style) {
      this.$refs.priceRange.$el.style.width = null
    }
  },
  components: {
    NavInPage,
    ProductCard
  },
  methods: {
    getSliderRangeData() {
      var arr = []
      for (var i = 0; i <= this.maxPrice; i = i + 10) {
        arr.push(i + '')
      }
      return arr
    }
  },
  computed: {
    sliderRangeData: function() {
      var arr = this.getSliderRangeData()
      console.log(arr)
      return arr
    }
  }
}
</script>

<style lang="sass" scoped>
</style>