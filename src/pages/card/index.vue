<template>
  <view>
    <view class="card-no-login">
      <span>为自己挑点儿喜欢的东西</span>

      <view style="display: flex;">
        <u-button shape="circle" size="mini">优惠活动</u-button>
        <u-button shape="circle" size="mini">立即登录</u-button>
      </view>
    </view>

    <y-recommend/>

  </view>
</template>

<script>
export default {
  data() {
    return {

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
