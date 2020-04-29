<template>
    <div :class="{
        'h-screen': true,
        'w-screen':true, 
        'bg-gray-300': bg_img?false:true,
    }"
    :style="{
        'background-image': `url(${bg_img})`
        }"
    >
        <div class="absolute top-0 right-0 w-full lg:w-1/2">
            <div class="flex h-screen">
                <div class="my-auto">
                    <slot name="content"></slot>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    props:{
        bg_img: String
    },
}
</script>