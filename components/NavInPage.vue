<template>
  <div class="inline-flex flex-row justify-start w-full mt-8">
    <!-- Refine list-->
    <nuxt-link class="refine-tag rounded-l" :class="{'active':isNewActive}" to="/new/">Newest</nuxt-link>
    <nuxt-link class="refine-tag" :class="{'active':isPopularActive}" to="/popular/">Popular</nuxt-link>
    <nuxt-link
      class="refine-tag"
      :class="{'active':isPriceRangeActive}"
      to="/priceRange/"
    >Price Range</nuxt-link>
    <nuxt-link class="refine-tag" :to="{ path: '/priceRange/', query: { to: '20' }}">Gifts Under $20</nuxt-link>
    <nuxt-link class="refine-tag rounded-r" :class="{'active':isRandomActive}" to="/random/">Random</nuxt-link>
  </div>
</template>

<script>
export default {
  props: ['active'],
  computed: {
    isNewActive: function() {
      return this.active === 'new'
    },
    isPopularActive: function() {
      return this.active === 'popular'
    },
    isPriceRangeActive: function() {
      return this.active === 'priceRange'
    },
    isRandomActive: function() {
      return this.active === 'random'
    }
  }
}
</script>

<style lang="sass">

.refine-tag
  @apply text-grey-darkest font-bold py-2 px-4 no-underline
  
  &:hover
    @apply text-white bg-blue 

  &:focus
    @apply outline-none

  &.active
    @apply text-white bg-blue

</style>