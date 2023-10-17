<template>
  <view class="y-product-card">
    <u--image  :showLoading="true" :src="product.image" width="100%" height="120px"/>
    <view class="y-product-card-body">
      <span class="y-product-card-title">{{ product.name }}</span>
      <view>
        <y-tag>{{ product.tag }}</y-tag>
      </view>
      <span class="y-product-card-price">${{ product.price }}</span>
    </view>

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
.y-product-card {
  width: inherit;
  margin: 4px;
  overflow: hidden;
  background: #fff;
  display: flex;
  border-radius: $y-radius;
  flex-direction: column;

  &-body{
    width: inherit;
    padding: 6px;
  }


  &-title {
    font-size: 1rem;
  }

  &-price {
    font-size: 1rem;
    color: red;
  }
}
</style>
