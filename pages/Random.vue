<template>
  <section class="container flex-col bg-white">
    <nav-in-page active="random"/>
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

</style>
