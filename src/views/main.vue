<script setup lang='ts'>
import { onMounted } from 'vue'
import * as L from 'leaflet'
import 'leaflet/dist/leaflet.css'

onMounted(() => {
    initMap()
})
// 地图初始化
const initMap = () => {
    const map = L.map('lMap').setView([51.505, -0.09], 13)
    L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
        maxZoom: 19,
        attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
    }).addTo(map)
}

</script>

<template>
    <div id="lMap">
    </div>
</template>

<style scoped>
#lMap {
    height: 100%;
}
</style>