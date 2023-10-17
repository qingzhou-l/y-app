<template>
  <view class="content">
    <u-sticky>
      <SearchBar/>
    </u-sticky>

    <u-swiper
        height="200"
        :list="list1"
    ></u-swiper>

    <NavMenu/>

    <y-activity-card title="今日好券" sub="领券">
      <y-coupon-card></y-coupon-card>
      <y-coupon-card></y-coupon-card>
      <y-coupon-card></y-coupon-card>
    </y-activity-card>
    <y-activity-card title="秒杀时刻">
      <template #title-sub>
        <u-count-down :time="30 * 60 * 60 * 1000" format="HH:mm:ss"></u-count-down>
      </template>
    </y-activity-card>
    <y-activity-card title="特惠拼团"></y-activity-card>

    <y-banner/>

    <u-tabs  :list="tabs"></u-tabs>

    <y-recommend/>
  </view>
</template>

<script>
import SearchBar from "@/pages/index/component/SearchBar.vue";
import NavMenu from "@/pages/index/component/NavMenu.vue";

export default {
  components: {NavMenu, SearchBar},
  data() {
    return {
      list1: [
        'https://cdn.uviewui.com/uview/swiper/swiper1.png',
        'https://cdn.uviewui.com/uview/swiper/swiper2.png',
        'https://cdn.uviewui.com/uview/swiper/swiper3.png',
      ],
      tabs:[
        {
          name:'为您推荐'
        },{
          name:'为您推荐'
        },{
          name:'为您推荐'
        },{
          name:'为您推荐'
        }
      ]
    }
  }
}
</script>

<style>

</style>
