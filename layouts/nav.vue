<template>
  <nav class="flex flex-col bg-white container">
    <div class="inline-flex flex-row items-center justify-between flex-wrap w-full p-6">
        <div class="flex items-center flex-no-shrink text-black mr-6">
            <svg
                class="fill-current h-8 w-8 mr-2"
                width="54"
                height="54"
                viewBox="0 0 54 54"
                xmlns="http://www.w3.org/2000/svg"
            >
                <path
                d="M13.5 22.1c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05zM0 38.3c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05z"
                ></path>
            </svg>
            <span class="font-semibold text-xl tracking-tight">Tailwind CSS</span>
        </div>
        <div class="w-full block flex-row-reverse flex-grow lg:flex lg:items-center lg:w-auto">
            <div>
                <!-- <input class="shadow appearance-none border rounded w-full py-2 px-3 text-grey-darker leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Username"> -->
                <input
                class="bg-grey-lighter appearance-none border-2 border-grey-lighter rounded w-full py-2 px-4 text-grey-darker leading-tight focus:outline-none focus:bg-white focus:border-blue"
                id="search"
                type="text"
                placeholder="Searching..."
                >
            </div>
        </div>
    </div>
    <div class="flex w-full">
        <!-- For Homepage -->
        <nuxt-link class="category" :class="colorList[0]" to="/new/">
        <!-- <i class="fas fa-home"></i> -->
            <p>HomePage</p>
        </nuxt-link>
        <!-- For Category -->
        <div class="category" v-for="(category, index) in categoryList" :key="category.id" :class="colorList[index+1]" >
            <!-- <i class="fas" :class="category.icon"></i> -->
            <p class="m-2">{{category.name}}</p>
        </div>
        <!-- For More -->
        <div class="category" :class="colorList[0]"> 
            <div class="inline-flex justify-center content-center">
                <i class="fas fa-bars"></i>
                <p class="ml-2">More</p>
            </div>
        </div>
    </div>
  </nav>
</template>

<script>
export default {
    data: function () {
    return {
        colorList: [
            "bg-grey hover:bg-grey-dark",
            "bg-red hover:bg-red-dark",
            "bg-orange hover:bg-orange-dark",
            "bg-yellow-dark hover:bg-yellow-darker",
            "bg-blue hover:bg-blue-darker",
            "bg-indigo hover:bg-indigo-darker",
        ],
        categoryList: [
            {
                "id": 1,
                "name": "Gifts For Male",
                "image": "",
            },
            {
                "id": 2,
                "name": "Gifts For Female",
                "image": ""
            },
            {
                "id": 3,
                "name": "Gifts For Geeky",
                "image": ""
            },
            {
                "id": 4,
                "name": "Gifts For Kid",
                "image": ""
            },
            {
                "id": 5,
                "name": "Gifts For Personalized",
                "image": ""
            }
        ]
    }
  }
}
</script>

<style scoped lang="sass">

.container 
  min-height: 0

.category 
    color: white
    @apply flex flex-col w-full py-2 cursor-pointer h-12 justify-center content-center no-underline font-bold
    justify-content: center

    &:hover 
        @apply border-b-4


</style>

