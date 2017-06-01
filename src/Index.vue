<template>
  <div id = "indexPage">
    <indexHeader></indexHeader>
    <indexLab></indexLab>
    <indexWork></indexWork>
    <b-map-component></b-map-component>
  </div>
</template>

<script>
import indexHeader from './component/index--header.vue'
import indexLab from './component/index--lab.vue'
import BMapComponent from './component/BMapComponent.vue'
import indexWork from './component/index--work.vue'
import indexSwiper from './component/index--swiper.vue'

// swiper options example:
export default {
  name: 'carrousel',
  data() {
    return {
     
    }
  },
   components: { indexHeader, indexLab, BMapComponent, indexWork, indexSwiper}
}

</script>
<style>
.index--container{
  box-sizing: border-box;
  width: 100%;
  min-height: 400px;
  background-size: cover;
  font-size:12px;
  line-height: 1.5;
  margin-bottom: 45px;
  position: relative;
}

</style>
