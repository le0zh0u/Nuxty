<template>
  <section class="container flex-row w-full">
    <div class="category-pannel">
      <category-list-pannel :current="$route.params.category"/>
    </div>
    <div class="card-pannel">
      <!-- category description -->
      <div class="w-full text-left mx-4 mt-2 mb-8">
        <div class="my-2">
          <!--category-title-->
          <h1>Man Cave Gifts</h1>
        </div>
        <div>
          <p
            class="text-xs leading-loose"
          >Every guy needs a man cave. But what do you fill it with besides a pool table, bar, and a big screen? The answer lies in this testosterone-laden man cave gift guide. With everything from a boxing glove bean bag chair to a DIY Heimlich maneuver tool, you’ll find everything necessary build the ultimate man cave.</p>
        </div>
      </div>
      <div
        class="inline-flex items-start w-ful justify-start bg-grey content-start text-left flex-wrap mb-2 py-4 px-2 mx-4"
      >
        <!-- sub category selector -->
        <div class="w-full md:w-1/4 px-3 mb-6 md:mb-0 my-2">
          <label
            class="block uppercase tracking-wide text-grey-darker text-xs font-bold mb-2"
            for="grid-state"
          >SubCarte</label>
          <div class="relative">
            <select
              class="block appearance-none w-full bg-grey-lighter border border-grey-lighter text-grey-darker py-3 px-4 pr-8 rounded leading-tight focus:outline-none focus:bg-white focus:border-grey"
              id="grid-state"
            >
              <option>New Mexico</option>
              <option>Missouri</option>
              <option>Texas</option>
            </select>
            <div
              class="pointer-events-none absolute pin-y pin-r flex items-center px-2 text-grey-darker"
            >
              <svg
                class="fill-current h-4 w-4"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
              >
                <path
                  d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"
                ></path>
              </svg>
            </div>
          </div>
        </div>
        <!-- sort by -->
        <div class="w-full md:w-1/4 px-3 mb-6 md:mb-0 my-2">
          <label
            class="block uppercase tracking-wide text-grey-darker text-xs font-bold mb-2"
            for="grid-state"
          >SortBy</label>
          <div class="relative">
            <select
              class="block appearance-none w-full bg-grey-lighter border border-grey-lighter text-grey-darker py-3 px-4 pr-8 rounded leading-tight focus:outline-none focus:bg-white focus:border-grey"
              id="grid-state"
            >
              <option>Popular</option>
              <option>Newest</option>
              <option>Low to High</option>
              <option>High to Low</option>
            </select>
            <div
              class="pointer-events-none absolute pin-y pin-r flex items-center px-2 text-grey-darker"
            >
              <svg
                class="fill-current h-4 w-4"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
              >
                <path
                  d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"
                ></path>
              </svg>
            </div>
          </div>
        </div>
        <div class="w-full md:w-1/4 px-3 mb-6 md:mb-0 my-2">
          <label
            class="block uppercase tracking-wide text-grey-darker text-xs font-bold mb-2"
            for="grid-first-name"
          >Min Price</label>

          <input
            class="appearance-none block w-full bg-grey-lighter text-grey-darker border border-grey-lighter rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-grey"
            id="grid-last-name"
            type="number"
            placeholder="Min"
          >
        </div>
        <div class="w-full md:w-1/4 px-3 mb-6 md:mb-0 my-2">
          <label
            class="block uppercase tracking-wide text-grey-darker text-xs font-bold mb-2"
            for="grid-first-name"
          >Max Price</label>
          <input
            class="appearance-none block w-full bg-grey-lighter text-grey-darker border border-grey-lighter rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-grey"
            id="grid-last-name"
            type="number"
            placeholder="Max"
          >
        </div>
        <div class="w-full px-3 md-6 md:mb-0 text-right">
          <button
            class="bg-blue hover:bg-blue-dark text-white font-bold py-2 px-4 mt-4 rounded uppercase"
          >Apply</button>
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
          img-url="https://cdn.thisiswhyimbroke.com/images/game-of-thrones-giant-paper-dragon-sculpture-youtube-viking-300x250.jpg"
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
        <product-card
          class="w-1/3 p-4"
          url
          af-url
          img-url="https://cdn.thisiswhyimbroke.com/images/game-of-thrones-giant-paper-dragon-sculpture-youtube-viking-300x250.jpg"
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
    </div>
  </section>
</template>

<script>
import CategoryListPannel from '~/components/categoryListPannel.vue'
import ProductCard from '~/components/ProductCard.vue'

export default {
  data: function() {
    return {}
  },
  components: { CategoryListPannel, ProductCard }
}
</script>

<style lang="sass" scoped>
.container 
    @apply justify-start content-start items-start my-4

    .category-pannel
        @apply w-1/4 border-solid border-r border-grey

    .card-pannel 
        @apply w-full flex flex-col flex

    .price-to
        @apply  mx-2 my-auto
</style>