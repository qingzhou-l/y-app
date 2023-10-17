<template>
  <view class="nav-menu">
    <u-grid col="5">
      <u-grid-item v-for="(item,index) in menu" :key="index">
        <view class="nav-menu-item">
          <u-icon :name="item.name"></u-icon>
          <text>{{ item.title }}</text>
        </view>
      </u-grid-item>
    </u-grid>
  </view>
</template>

<script>
export default {
  data() {
    return {
      menu: [
        {
          name: 'eye',
          title: '数码'
        }, {
          name: 'eye',
          title: '数码'
        }, {
          name: 'eye',
          title: '数码'
        }, {
          name: 'eye',
          title: '数码'
        }, {
          name: 'eye',
          title: '数码'
        }, {
          name: 'eye',
          title: '数码'
        }, {
          name: 'eye',
          title: '数码'
        }, {
          name: 'eye',
          title: '数码'
        }, {
          name: 'eye',
          title: '数码'
        }, {
          name: 'eye',
          title: '数码'
        }
      ]
    };
  }
}
</script>

<style lang="scss">

.nav-menu{
  margin: 12px 0;
  &-item{
    margin: 10px 0;
  }
}

</style>
