<template>
  <view class="my">
    <view class="my-setting">
      <u-icon size="20px" name="setting-fill"></u-icon>
      <u-icon size="20px" name="chat-fill"></u-icon>
    </view>

    <view class="my-no-login">
      <view class="my-info flex center">
        <u-avatar size="46"
                  src="https://img2.baidu.com/it/u=3892566647,2527220612&fm=253&app=138&size=w931&n=0&f=JPEG&fmt=auto?sec=1697562000&t=3da69af1da623ac40793e010e222710d"></u-avatar>
        <text>未登录</text>
      </view>
      <u-icon name="arrow-right" size="18"/>
    </view>

    <ActivityArea/>

    <OrderArea/>
    <ServeArea/>
    <y-banner/>
    <y-recommend/>
  </view>
</template>

<script>
import OrderArea from "@/pages/my/component/OrderArea.vue";
import ServeArea from "@/pages/my/component/ServeArea.vue";
import ActivityArea from "@/pages/my/component/ActivityArea.vue";

export default {
  components: {ActivityArea, ServeArea, OrderArea},
  data() {
    return {};
  }
}
</script>

<style lang="scss">
.my {
  &-setting {
    margin-left: calc(100% - (60px + 12px));
    width: 60px;
    display: flex;
    justify-content: space-between;
    padding: 4px 0;
  }

  &-info {
    text {
      margin-left: 12px;
      font-size: 1rem;
      font-weight: 400;
    }
  }

  &-no-login {
    margin: 12px;
    display: flex;
    justify-content: space-between;
  }
}
</style>
