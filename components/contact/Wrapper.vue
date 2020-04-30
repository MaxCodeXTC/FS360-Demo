<template>
    <div class="grid grid-cols-1 md:grid-cols-2">
        <div class="h-full">
            <leaftletMap />
        </div>
        <div class="px-2 md:px-20">
            <contactForm/>
        </div>
    </div>
</template>
<script>
import ContactForm from '~/components/contact/Form.vue'
import Map from '~/components/contact/Map.vue'

export default {
    components:{
        contactForm : ContactForm,
        leaftletMap: Map
    }
}
</script>