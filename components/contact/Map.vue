<template>
    <div class="relative">
        <div style="height:450px">
            <div id="map-wrap" class="pl-10 h-full w-full">
                <client-only>      
                    <l-map 
                        :zoom="16" 
                        :center="[3.152596, 101.622784]" 
                        :options="{
                            zoomControl:false,
                            dragging: false,
                            boxZoom: false,
                            doubleClickZoom: false,
                            minZoom: 16,
                            maxZoom:16
                        }"
                        >
                        <l-tile-layer :url="mapUrl" attribution='&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'></l-tile-layer>
                        <l-marker
                            :lat-lng="[3.152596, 101.622784]"
                            @add="openPopup"
                        >
                            <l-popup :lat-lng="[3.152596, 101.622784]"
                                :options="{
                                    keepInView: true,
                                    closeButton: false,
                                    autoClose: false,
                                    closeOnEscapeKey: false,
                                    closeOnClick:false
                                }"
                            >
                                <div class="flex flex-col w-64 h-full items-center">
                                    <div class="h-12 w-12">
                                        <img class="h-full w-full object-cover" src="~/assets/img/lead.png"/>
                                    </div>
                                    <div class="text-left py-2 px-6">
                                         Level 11, Menara KEN TTDI, No.37 Jalan Burhanuddin Helmi, Taman Tun Dr. Ismail
                                    </div>
                                    <div class="text-sm font-sans">
                                        <a class="text-left hover:text-blue-700 hover:no-underline" href="https://thelead.io">https://thelead.io</a>
                                    </div>
                                </div>
                            </l-popup>
                        </l-marker>
                    </l-map>
                </client-only>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data: () =>{
        return {
            mapUrl: "https://{s}.basemaps.cartocdn.com/rastertiles/voyager/{z}/{x}/{y}{r}.png"
        }
    },
    methods:{
        openPopup(event){
            this.$nextTick(()=>{
                    event.target.openPopup();
                }
            );
        },
    }
}
</script>