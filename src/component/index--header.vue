<template>
  <div class = 'index--pic--change index--container'>
     <div class = 'index--pic--des'>
        <p class = 'index--pic--title'>
          {{ describe[0].title }}
        </p>
        <small class = 'index--pic--subtitle'> 
          {{ describe[0].subtitle }} 
        </small>
     </div>
  </div>
</template>
 
<script>
import Swiper from 'vue-swiper'
export default {
  data() {
    return {
      describe:[
        {
          "title": "2016届设计实践作品展顺利举行",
          "subtitle": "这些是简单的说明文字这些是简单的说明文字这些是简单的说明文字这些是简单的说明文字这些是简单的说明文字"
        }
      ],
      components:{ Swiper },
      methods: {
        onSlideChangeStart (currentPage) {
            console.log('onSlideChangeStart', currentPage);
        },
        onSlideChangeEnd (currentPage) {
            console.log('onSlideChangeEnd', currentPage);
        }
    }
    }
  }
}

</script>
 
<style>
.index--pic--change{
  background-image: url('../assets/index--header--img.png');
}
.index--pic--des{
  color: #ffffff;
  margin: 0 auto;
  width: 80%;
}
.index--pic--title{
  position: absolute;
  bottom: 8%;
  font-size: 20px;
  margin-bottom: 24px;
}
.index--pic--subtitle{
  position: absolute;
  bottom: 5%;
  font-size: 12px;
}

</style>