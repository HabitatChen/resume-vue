<template>
    <div class="wrapper">
      <h2>作品集</h2>
      <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide  v-for="item of list" :key="item.id">
          <img class="swiper-img" :src="item.imgUrl" alt=""></swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>

</template>

<script>
import appleAlike from '@/assets/apple-style-slides.jpg'
import canvas from '@/assets/canvas.jpg'
import navPage from '@/assets/nav-page.jpg'

export default {
  name: "HomeProject",
  data: function() {
    return {
      swiperOption: {
        autoplay: true,
        pagination: {
            el:'.swiper-pagination',
            type:'progressbar'
        },
        loop:true,
      },
      list:[{
          id:'0001',
          imgUrl:appleAlike
      },{
          id:'0002',
          imgUrl:canvas
      },{
          id:'0003',
          imgUrl:navPage
      }]
    }
  },
  computed: {
  }
};
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination
    background: white 
.wrapper {
    width:100%
    height:740px;
    width 940px
    margin 75px auto
    .swiper-img {
        width: 100%;
    }
}
.wrapper h2,
{
  text-align: center;
  color: #3d4451;
  font-size: 34px;
  line-height: 1.2;
  font-weight: 600;
  margin-bottom 40px
}
.wrapper swiper 
    background red
</style>
