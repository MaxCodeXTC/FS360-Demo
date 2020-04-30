<template>
    <div class="h-full w-screen">
        <div class="flex flex-col">
            <grid2>
                <template v-slot:content_1>
                    <div class="flex">
                    <div class="m-auto p-4">
                        <div class="font-sans font-light text-5xl text-gray-700 tracking-widest">MORE THAN</div> 
                        <div class="font-sans font-bold text-5xl text-gray-700" style="margin-top:-20px;">RESPONSIVE</div>
                        <div class="w-12 bg-gray-700 separator-line" style="margin-top:1px !important"></div>
                        <div class="mt-5 w-4/5">
                        <p class="font-serif font-hairline text-gray-500 text-sm">
                            Sed ut perspiciatis unde omnis iste nat eror acus antium que. Asperiores, ea velit enim labore doloribus.
                        </p>
                        </div>
                    </div> 
                    </div>
                </template>
                <template v-slot:content_2>
                    <div >
                    <img src="~/assets/img/grid_1.jpg"/>
                    </div>
                </template>
                </grid2>
                
                <grid2>
                <template v-slot:content_1>
                    <div >
                    <img src="~/assets/img/grid_2.jpg"/>
                    </div>
                </template>
                <template v-slot:content_2>
                    <div class="flex">
                    <div class="m-auto">
                        <div class="font-sans font-light text-5xl text-gray-700 tracking-widest">POWERFUL</div> 
                        <div class="font-sans font-bold text-5xl text-gray-700" style="margin-top:-20px;">PERFORMANCE</div>
                        <div class="w-12 bg-gray-700 separator-line" style="margin-top:1px !important"></div>
                        <div class="mt-5 w-4/5">
                        <p class="font-serif font-hairline text-gray-500 text-sm">
                            Sed ut perspiciatis unde omnis iste nat eror acus antium que. Asperiores, ea velit enim labore doloribus.
                        </p>
                        </div>
                    </div> 
                    </div>
                </template>
            </grid2>
        </div>
    </div>
</template>
<script>
import Grid2 from "~/components/content/Grid2.vue";

export default {
    components:{
        grid2: Grid2,
    }
}
</script>