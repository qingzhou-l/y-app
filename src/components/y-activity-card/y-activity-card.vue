<template>
  <view class="y-activity-card">
    <view class="y-activity-card-header">
      <view class="y-activity-card-theme">
        <span class="y-activity-card-title">{{title}}</span>
        <slot name="title-sub"></slot>
      </view>
      <view class="y-activity-card-sub">
        <span>{{sub}}</span>
        <u-icon name="arrow-right"/>
      </view>
    </view>

    <view class="y-activity-card-body">
      <slot/>
    </view>
  </view>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: '默认标题',
      // required: true
    },
    sub: {
      type: String,
      default: '查看全部'
    }
  },
  data() {
    return {};
  }
}
</script>

<style lang="scss">
.y-activity-card {
  margin: 12px;
  padding: 12px;
  border-radius: $y-radius;

  &-title{
    font-size: 14px;
    font-weight: 600;
  }


  &-theme,&-header,&-sub{
    display: flex;
    flex-direction: row;
    flex-flow: nowrap;
    justify-content: space-between;
    align-items: center;
  }


  &-body{
    margin-top: 12px;
    display: flex;
    overflow-y: auto;
  }
}
</style>
