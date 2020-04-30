<template>
    <div class="relative cursor-pointer">
        <div>
            <div class="block overflow-hidden">
                <img :class="{
                    'transition':true, 
                    'duration-500':true, 
                    'ease-in-out':true, 
                    'transform':true,
                    '-translate-y-1':hover,
                    'scale-125':hover,
                    'object-cover':true,
                    }" :src="img_url">
                <!-- <slot name="img"></slot> -->
            </div>
            <div class="absolute w-full h-full top-0" @mouseover="hover=true" @mouseleave="hover=false">
                <div :class="{
                    'flex': true,
                    'h-full': true,
                    'transition':true, 
                    'duration-500':true, 
                    'ease-in-out':true, 
                    'product-hover': hover
                    }">
                    <div class="my-auto px-10" v-if="hover">
                        <div class="text-white font-bold text-3xl font-sans tracking-wide">
                            <slot name="name"></slot>
                        </div>
                        <div class="text-white font-light text-md font-sans">
                            <slot name="description"></slot>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data: () => {
        return {
            hover: false
        }
    },
    props: {
        img_url: String
    }
}
</script>
<style>
.product-hover{
    background-color: rgb(0,0,0,.8)
}
</style>