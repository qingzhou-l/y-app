<template>
  <view class="nav-menu">
    <u-grid col="5">
      <u-grid-item v-for="item in menu" :key="item.id">
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
          id:'1',
          name: 'eye',
          title: '数码'
        }, {
          id:'2',
          name: 'eye',
          title: '数码'
        }, {
          id:'3',
          name: 'eye',
          title: '数码'
        }, {
          id:'4',
          name: 'eye',
          title: '数码'
        }, {
          id:'5',
          name: 'eye',
          title: '数码'
        }, {
          id:'6',
          name: 'eye',
          title: '数码'
        }, {
          id:'7',
          name: 'eye',
          title: '数码'
        }, {
          id:'8',
          name: 'eye',
          title: '数码'
        }, {
          id:'9',
          name: 'eye',
          title: '数码'
        }, {
          id:'10',
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
