<template>
  <view class="y-tag">
    <small>
      <slot/>
    </small>
  </view>
</template>

<script>
export default {
  data() {
    return {};
  }
}
</script>

<style lang="scss">
.y-tag {
  display: inline-block;
  background: #f8dada;
  padding: 2px 4px;
  border-radius: $y-radius;
  transform: scale(.8);
}
</style>
