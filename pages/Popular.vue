<template>
  <section class="container flex-col bg-white">
    <nav-in-page active="popular"/>
    <div class="flex flex-row flex-wrap w-full justify-start">
      <!-- recommend list -->
      <product-card class="w-1/3 p-4" url="" af-url="" img-url="https://tailwindcss.com/img/card-top.jpg" title="The Coldest Sunset" desc="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil."/>
      <product-card class="w-1/3 p-4" url="" af-url="" img-url="https://tailwindcss.com/img/card-top.jpg" title="The Coldest Sunset" desc="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil."/>
      <product-card class="w-1/3 p-4" url="" af-url="" img-url="https://tailwindcss.com/img/card-top.jpg" title="The Coldest Sunset" desc="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil."/>
      <product-card class="w-1/3 p-4" url="" af-url="" img-url="https://tailwindcss.com/img/card-top.jpg" title="The Coldest Sunset" desc="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil."/>
    </div>
  </section>
</template>

<script>
import NavInPage from '~/components/NavInPage.vue'
import ProductCard from '~/components/ProductCard.vue'

export default {
  components: {
    NavInPage, ProductCard
  }
}
</script>

<style lang="sass">

.title 
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif
  display: block
  font-weight: 300
  font-size: 100px
  color: #35495e
  letter-spacing: 1px

.subtitle 
  font-weight: 300
  font-size: 42px
  color: #526488
  word-spacing: 5px
  padding-bottom: 15px

.links 
  padding-top: 15px

</style>
