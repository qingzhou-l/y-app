<template>
  <view class="y-recommend">
    <u-divider :text="title"/>
    <view class="y-recommend-content">
      <y-product-card :product="products[0]"/>
      <y-product-card :product="products[0]"/>
      <y-product-card :product="products[0]"/>
      <y-product-card :product="products[0]"/>
      <y-product-card :product="products[0]"/>
    </view>

  </view>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: false,
      default: '猜你喜欢'
    }
  },
  data() {
    return {
      products: [
        {
          name: 'hhh',
          image: 'https://img2.baidu.com/it/u=3892566647,2527220612&fm=253&app=138&size=w931&n=0&f=JPEG&fmt=auto?sec=1697562000&t=3da69af1da623ac40793e010e222710d',
          price: 123.99,
          tag: '第二份半价'
        }
      ]
    };
  }
}
</script>

<style lang="scss">
.y-recommend{
  margin: 12px;

  &-content{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 6px;
  }
}

</style>
