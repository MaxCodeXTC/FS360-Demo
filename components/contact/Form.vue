<template>
    <div>
        <form class="bg-white shadow-md rounded px-6 pt-10 pb-12 mb-4">
            <div class="flex mb-5 items-center">
                <div class="w-1 h-10 bg-gray-700 mr-4"></div>
                <div class="text-gray-700 text-2xl font-thin font-sans tracking-wider mr-2">CONTACT</div>
                <div class="text-gray-700 text-2xl font-bold font-sans tracking-wider"> US</div>
            </div>
            <div class="mb-3">
                <inputElement :labelName="'Username'" :labelId="'username'" :focus="false" :value="username" @input="username = $event" />
            </div>
            <div class="mb-3">
                <inputElement :labelName="'Email'" :labelId="'email'" :focus="false" :value="email" @input="email = $event" />
            </div>
            <div class="mb-3">
                <textElement :labelName="'Content'" :labelId="'content'" :focus="false" :value="content"  :disabled="false"/>
            </div>
            <div class="flex items-center justify-between">
                <button class="
                    bg-gray-500  
                    w-full
                    text-white 
                    font-bold 
                    py-2 
                    px-4 
                    rounded
                    transition
                    duration-200
                    hover:bg-gray-700
                    focus:outline-none 
                    focus:shadow-outline" 
                    type="button">
                    Submit
                </button>
            </div>
        </form>
    </div>
</template>
<script>
import inputElement from '~/components/items/Input.vue'
import textElement from '~/components/items/TextArea.vue';

export default {
    components:{
        inputElement,
        textElement
    },
    data: () => {
        return{
            errorMsg: "",
            username: "",
            email: "",
            content:""
        }
    }
}
</script>