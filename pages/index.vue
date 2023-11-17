<template>
  <!-- กำหนดพื้นที่ของแผนที่บนเว็บ  -->
  <div style="height: 100dvh" id="map"></div>
</template>

<script>
export default {
  data() {
    return {
      zoom: 6,
      center: [14.870032, 102.992541],
      map: null,
    }
  },
  methods: {
    initmap() {
      const map = L.map('map').setView(this.center, this.zoom)
      this.map = map

      L.tileLayer(
        'https://api.maptiler.com/maps/basic-v2/{z}/{x}/{y}.png?key=ODQYjrfwMX2CleHUV2jQ'
      ).addTo(map)
    },
  },
  mounted() {
    this.initmap()
  },
}
</script>

<style>
</style>