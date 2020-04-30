<template>
  <div>
    <navi />
    <contentWrapper id="home" :bg_img="'../img/bg_1.jpg'">
      <template v-slot:content>
        <div class="lg:pl-20 pb-20">
            <div class="font-sans font-light text-8xl text-white transition duration-500 ease-in-out lg:text-gray-800">Begin</div>
            <div class="font-sans font-bold text-8xl text-white transition duration-500 ease-in-out lg:text-gray-800 sub-topic">Anywhere</div>
            <div class="w-20 bg-white transition duration-500 ease-in-out lg:bg-gray-800 separator-line"></div>
            <div class="font-sans font-thin text-3xl text-white transition duration-500 ease-in-out lg:text-gray-800 description">Your passion will guide you</div>
        </div>
      </template>
    </contentWrapper>
    <gridWrapper id="features" />
    <productWrapper id="products" />
    <aboutus id="aboutus"/>
    <contactWrapper id="contactus"/>
    <footerWrapper />
  </div>
</template>

<script>
import Navi from "~/components/navi/Wrapper.vue";
import ContentWrapper from "~/components/content/ImageWrapper.vue";
import GridWrapper from "~/components/content/GridWrapper.vue";
import ProductWrapper from "~/components/content/ProductWrapper.vue";
import AboutUs from "~/components/content/AboutUs.vue";
import ContactWrapper from "~/components/contact/Wrapper.vue";
import FooterWrapper from "~/components/footer/Wrapper.vue";

export default {
  components: {
    navi : Navi,
    contentWrapper: ContentWrapper,
    gridWrapper: GridWrapper,
    productWrapper: ProductWrapper,
    aboutus: AboutUs,
    contactWrapper: ContactWrapper,
    footerWrapper: FooterWrapper
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
