<template>
  <view>
    <u--image :showLoading="true" :src="product.image" width="80px" height="80px"/>
    <span>{{ product.name }}</span>
    <u-tag  :text="product.tag" plain shape="circle"></u-tag>
    <span>${{ product.price }}</span>
  </view>
</template>

<script>
export default {
  props: ['product'],
  data() {
    return {};
  }
}
</script>

<style lang="scss">
.y-product-card{
  width: 200px;
}
</style>
