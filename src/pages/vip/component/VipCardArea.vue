<template>
  <view class="vip-card-area">
    <u-subsection mode="button" @change="changeCurrent" key-name="title" :list="grade" :current="current"></u-subsection>

    <view>
      <template v-for="(item,key) in grade">
        <view class="vip-card-content" v-show="key===current">
          <view class="flex column">
            <text class="vip-card-title">
              {{ item.title }}
            </text>
            <small class="vip-card-sub">
              加入{{ item.day }}，已省￥{{ item.save }}
            </small>
          </view>

          <view>
            <u-grid col="4">
              <u-grid-item v-for="(child,index) in item.privilege" :key="index">
                <view class="flex column center">
                  <u-icon name="qzone" color="#fff" size="24"></u-icon>
                  <text style="color: #fff">{{ child.title }}</text>
                  <text class="vip-card-sub">{{ child.sub }}</text>
                </view>
              </u-grid-item>
            </u-grid>
          </view>
        </view>

      </template>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      grade: [
        {
          title: '黄金VIP',
          day: 12314,
          save: 123423.99,
          privilege: [
            {
              title: '会员专享价',
              sub: '预计省￥569'
            }, {
              title: '会员专享价',
              sub: '预计省￥569'
            }, {
              title: '会员专享价',
              sub: '预计省￥569'
            }, {
              title: '会员专享价',
              sub: '预计省￥569'
            }
          ]
        }, {
          title: '铂金VIP',
          day: 12314,
          save: 123423.99,
          privilege: [
            {
              title: '会员专享价',
              sub: '预计省￥569'
            }, {
              title: '会员专享价',
              sub: '预计省￥569'
            }, {
              title: '会员专享价',
              sub: '预计省￥569'
            }, {
              title: '会员专享价',
              sub: '预计省￥569'
            }
          ]
        }, {
          title: '钻石VIP',
          day: 12314,
          save: 123423.99,
          privilege: [
            {
              title: '会员专享价',
              sub: '预计省￥569'
            }, {
              title: '会员专享价',
              sub: '预计省￥569'
            }, {
              title: '会员专享价',
              sub: '预计省￥569'
            }, {
              title: '会员专享价',
              sub: '预计省￥569'
            }
          ]
        },
      ],
      current: 0,
    };
  },
  methods: {
    changeCurrent(key) {
      this.current = key
    }
  },
}
</script>

<style lang="scss">
.vip-card-area {
  .vip-card-title {
    font-size: 1.5rem;
    font-weight: 700;
    color: #fff;
  }

  .vip-card-sub {
    color: $y-text-gray;
  }
}


.vip-card-content {
  margin: 12px;
  min-height: 160px;
  display: flex;
  flex-direction: column;
  border-radius: 10px;
  overflow: hidden;
  justify-content: space-between;
  padding: 12px;
  background-color: #413f3f;

}
</style>
