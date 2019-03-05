<template>
<div class="wrapper">
  <swiper :options="swiperOption" >
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-image" :src="item.imgUrl" alt="">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '001',
        imgUrl: 'http://img.netbian.com/file/newc/d9c5953af524e8d0096237cf143839da.jpg'
      }, {
        id: '002',
        imgUrl: 'https://imgs.qunarzz.com/p/tts8/1703/94/61eb7ce216efc702.jpg_r_390x260x90_d5dd6341.jpg'
      }, {
        id: '003',
        imgUrl: 'http://img.netbian.com/file/newc/00979469b777cfc8e1c7650fdd3fc481.jpg'
      }]
    }
  }
}
</script>
<style scoped>
.wrapper >>> .swiper-pagination-bullet-active{
    background: white;
}
.wrapper{
    width: 100%;
    height: 0;
    overflow: hidden;
    padding-bottom: 2.74rem;
    background: #eee;
}
.swiper-image{
    width: 100%;
    height: 2.74rem;
}
</style>
