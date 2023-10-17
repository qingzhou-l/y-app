<template>
  <view class="y-card">
    <view v-if="title">
      <text class="y-card-title">{{ title }}</text>
    </view>
    <view>
      <slot/>
    </view>

  </view>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: false
    }
  },
  data() {
    return {};
  }
}
</script>

<style lang="scss">
.y-card {
  margin: 12px;
  padding: 12px;
  min-width: inherit;
  border-radius: $y-radius;
  overflow: hidden;
  background: #fff;

  &-title{
    font-size: 1rem;
    font-weight: 600;
  }
}
</style>
