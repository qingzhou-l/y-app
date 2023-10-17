<template>
  <view class="h-full">
    <view class="classify-search">
      <u-search bg-color="#fff"></u-search>
    </view>

    <view class="classify-content">
      <SideMenu :menus="menus" default-key="数码"/>
      <view class="classify-product">
        <ProductArea/>
      </view>

    </view>

  </view>
</template>

<script>
import SideMenu from "@/pages/classify/component/SideMenu.vue";
import ProductArea from "@/pages/classify/component/ProductArea.vue";

export default {
  components: {ProductArea, SideMenu},
  data() {
    return {
      menus: [
        {
          label: '数码',
          key: '数码'
        }, {
          label: '母婴',
          key: '母婴'
        },
      ]
    };
  }
}
</script>

<style lang="scss">
.classify-search {
  padding: 0 12px;
}

.classify-content {
  height: inherit;
  display: flex;
}

.classify-product {
  width: 100%;
  margin-left: 92px;
}
</style>
