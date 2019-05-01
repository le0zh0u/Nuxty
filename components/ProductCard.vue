<template>
    <div>
        <div class="max-w-sm rounded overflow-hidden hover:shadow-lg">
            <img class="w-full cursor-pointer " :src="imgUrl">
            <div class="px-4 py-2">
                <div class="font-bold text-grey-darkest mb-2 h-6 leading-normal hover:text-orange cursor-pointer text-left text-lg">{{title}}</div>
                <p class="description">
                    {{desc}}
                </p>
            </div>
            <div class="px-4 py-4">
                <div>
                    <!-- share -->

                </div>
                <button class="hover:bg-orange bg-orange-light text-white font-bold py-2 px-4 border-b-4 hover:border-orange-dark border-orange rounded">
                    Check it out
                </button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "ProductCard",
        data: function() {
            return {

            }
        },
        props: [
            'imgUrl', 'title', 'desc', 'url', 'afUrl'
        ]
    }
</script>

<style lang="sass" scoped>

.description 
    @apply text-grey-darker text-base cursor-default text-left h-16 text-xs
    display: -webkit-box
    overflow: scroll
</style>