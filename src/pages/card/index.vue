<template>
  <view>
    <view class="card-no-login">
      <span>为自己挑点儿喜欢的东西</span>

      <view style="display: flex;">
        <u-button shape="circle" size="mini">优惠活动</u-button>
        <u-button shape="circle" size="mini">立即登录</u-button>
      </view>
    </view>


    <u-divider text="猜你喜欢"/>

    <y-product-card v-for="item in products" product="item"/>
  </view>
</template>

<script>
export default {
  data() {
    return {
      products:[
        {
          name:'hhh',
          image:'https://img2.baidu.com/it/u=3892566647,2527220612&fm=253&app=138&size=w931&n=0&f=JPEG&fmt=auto?sec=1697562000&t=3da69af1da623ac40793e010e222710d',
          price:123.99
        }
      ]
    };
  }
}
</script>

<style lang="scss">
.card-no-login{
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;

  span{
    margin: 12px 0;
  }
}
</style>
