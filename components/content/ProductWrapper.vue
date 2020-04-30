<template>
    <div class="py-4 w-screen">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
            <product :img_url="'../img/product-1.jpg'">
                <template v-slot:name>
                    PRODUCT 1
                </template>
                <template v-slot:description>
                    Product Type / Product Description
                </template>
            </product>
            <product :img_url="'../img/product-2.jpg'">
                <template v-slot:name>
                    PRODUCT 2
                </template>
                <template v-slot:description>
                    Product Type / Product Description
                </template>
                </product>
            <product :img_url="'../img/product-3.jpg'">
                <template v-slot:name>
                    PRODUCT 3
                </template>
                <template v-slot:description>
                    Product Type / Product Description
                </template>
            </product>
            <product :img_url="'../img/product-4.jpg'">
                <template v-slot:name>
                    PRODUCT 4
                </template>
                <template v-slot:description>
                    Product Type / Product Description
                </template>
            </product>
            <product :img_url="'../img/product-5.jpg'">
                <template v-slot:name>
                    PRODUCT 5
                </template>
                <template v-slot:description>
                    Product Type / Product Description
                </template>
            </product>
            <product :img_url="'../img/product-6.jpg'">
                <template v-slot:name>
                    PRODUCT 6
                </template>
                <template v-slot:description>
                    Product Type / Product Description
                </template>
            </product>
        </div>
    </div>
</template>
<script>
import Product from "~/components/content/Product.vue";

export default {
    components:{
        product: Product,
    }    
}
</script>