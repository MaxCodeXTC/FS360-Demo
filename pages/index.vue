<template>
  <div>
    <navi />
    <contentWrapper :bg_img="'../img/bg_1.jpg'">
      <template v-slot:content>
        <div class="lg:pl-20 pb-20">
            <div class="font-sans font-light text-8xl text-white transition duration-500 ease-in-out lg:text-gray-800">Begin</div>
            <div class="font-sans font-bold text-8xl text-white transition duration-500 ease-in-out lg:text-gray-800 sub-topic">Anywhere</div>
            <div class="w-20 bg-white transition duration-500 ease-in-out lg:bg-gray-800 separator-line"></div>
            <div class="font-sans font-thin text-3xl text-white transition duration-500 ease-in-out lg:text-gray-800 description">Your passion will guide you</div>
        </div>
      </template>
    </contentWrapper>
    <gridWrapper>
      <template v-slot:content>
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
      </template>
    </gridWrapper>
    <productWrapper>
      <template v-slot:products>
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
      </template>
    </productWrapper>
  </div>
</template>

<script>
import Navi from "~/components/navi/Wrapper.vue"
import ContentWrapper from "~/components/content/ImageWrapper.vue"
import GridWrapper from "~/components/content/GridWrapper.vue"
import Grid2 from "~/components/content/Grid2.vue"
import ProductWrapper from "~/components/content/ProductWrapper.vue"
import Product from "~/components/content/Product.vue"

export default {
  components: {
    navi : Navi,
    contentWrapper: ContentWrapper,
    gridWrapper: GridWrapper,
    grid2: Grid2,
    productWrapper: ProductWrapper,
    product: Product
  }
}
</script>
<style>

.sub-topic{
    margin-top:-40px;
    margin-left:20px;
}
.separator-line{
    margin-top: -15px;
    margin-left:-5px;
    height:2px;
}
</style>
