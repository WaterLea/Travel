<template>
    <div class=icons>
         <swiper >
            <swiper-slide  v-for="(page,index) of pages" :key="index">
                <div class="icon" v-for="item of page"
                :key="item.id" >
                    <div class="icon-img">
                        <img class="icon-img-content" :src="item.imgUrl" alt="">
                    </div>
                    <p class="icon-desc">{{item.desc}}</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>
<script>

export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [ {
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        desc: '一日游'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
        desc: '识春赏花'
      }, {
        id: '004',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20191/de711920c71e38287d9f95f7910aa1aa.png',
        desc: '精品小团'
      }, {
        id: '005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
        desc: '重庆'
      }, {
        id: '006',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
        desc: '动植物园'
      }, {
        id: '007',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: '008',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
        desc: '一日游'
      }, {
        id: '009',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
        desc: '泡温泉'
      }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style scoped>
.icons .swiper-container{
    height: 0;
    padding-bottom: 50%;
}
.icon{
    float: left;
    width: 25%;
    height: 0;
    padding-bottom: 25%;
    position: relative;
    overflow: hidden;
}
.icon-img{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0.44rem;
    margin:0 auto;
    box-sizing: border-box;
    padding: 0.1rem;
}
.icon-img-content{
   height:100% ;
   display: block;
   margin: 0 auto;
}
.icon-desc{
    position:absolute;
    left:0;
    right:0;
    bottom:0.1rem;
    text-align: center;
    color: #333;
}
</style>
