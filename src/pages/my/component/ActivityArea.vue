<template>
  <y-card>
    <u-grid :border="true" col="3">
      <u-grid-item v-for="item in lists" :key="item.id">
        <view class="activity-content">
          <view class="flex column" style="margin-right: 6px">
            <text class="activity-title">{{ item.title }}</text>
            <text class="activity-sub">{{ item.sub }}</text>
          </view>
          <u-avatar/>
        </view>
      </u-grid-item>
    </u-grid>
  </y-card>
</template>

<script>
export default {
  data() {
    return {
      lists: [
        {
          id: 1,
          title: '红包卡券',
          sub: '领券中心'
        }, {
          id: 2,
          title: '红包卡券',
          sub: '领券中心'
        }, {
          id: 3,
          title: '红包卡券',
          sub: '领券中心'
        },
      ]
    };
  }
}
</script>

<style lang="scss">
.activity-content {
  display: flex;
  align-items: center;

  .activity-sub{
    color:$y-text-gray
  }


}
</style>
