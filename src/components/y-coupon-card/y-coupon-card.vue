<template>
  <view class="y-coupon-card">
    <view class="y-coupon-card-info">
      <span>
        <strong>${{ money }}</strong>
      </span>
      <view>
        <span>无门槛</span>
        <p>指定商品可用</p>
      </view>
    </view>

    <u-line dashed color="#000" ></u-line>

    <view class="y-coupon-card-draw">
      <view class="y-coupon-card-btn">
        <span>立即领取</span>
        <u-icon color="#fff" name="arrow-right" />
      </view>
    </view>
  </view>
</template>

<script>
export default {
  props: {
    money: {
      type: Number,
      default: 99
    }
  },
  data() {
    return {};
  }
}
</script>

<style lang="scss">
.y-coupon-card {
  margin-right: 12px;
  min-width: 130px;
  padding: 12px;
  border-radius: $y-radius;
  background: rgb(234, 236, 242);
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;

  &-info {
    display: flex;
    justify-content: center;
    align-items: flex-end;

    strong{
      font-size: 18px;
    }

    >view{
      margin-left: 6px;

      p{
        color: $y-text-gray;
      }
    }

  }


  &-btn{
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 6px;
    background: red;
    padding: 2px 4px;
    color: #fff;
    border-radius: $y-radius;
  }
}
</style>
