<template>
  <div class="category-list-pannel">
    <div class="font-bold my-2" v-for="category in categoryList" :key="category.id">
      <nuxt-link
        class="text-base hover:text-orange cursor-pointer text-black no-underline"
        :class="{'active':isActive(category.slug)}"
        :to="category.slug"
      >{{category.title}}</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      categoryList: [
        {
          id: 1,
          title: 'Gear + Gadgets',
          description: 'Tet',
          slug: 'gear-and-gadgets',
          parent: 0
        },
        {
          id: 2,
          title: 'Gifts For Men',
          description: 'Test',
          slug: 'gifts-for-men',
          parent: 0
        },
        {
          id: 3,
          title: 'Gifts For Women',
          description: 'Test',
          slug: 'gifts-for-women',
          parent: 0
        },
        {
          id: 4,
          title: 'Gifts For Kids',
          description: 'Tet',
          slug: 'gifts-for-kids',
          parent: 0
        },
        {
          id: 5,
          title: 'Gifts For Geeky',
          description: 'Tet',
          slug: 'gifts-for-geeky',
          parent: 0
        }
      ]
    }
  },
  props: ['current'],
  methods: {
    isActive(slug) {
      console.log(this.current)
      if (this.current === slug) {
        return true
      }
      return false
    }
  }
}
</script>

<style lang="sass" scoped>

.category-list-pannel
    @apply flex flex-col justify-start

.active
    @apply text-orange
</style>