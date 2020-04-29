<template>
    <div class="absolute w-full top-0 z-10">
        <div class="flex justify-between px-8 pt-8 pb-4 items-center">
            <div>
                <img class="w-32" src="~/assets/img/logo.png" />
            </div>
            <menuList />
        </div>
    </div>
</template>
<script>
import Menu from '~/components/navi/Menu.vue'

export default {
    name:"MenuWrapper",
    components:{
        menuList: Menu
    }    
}
</script>