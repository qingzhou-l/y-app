<template>
  <view class="search-bar">
    <u-row gutter="10">
      <u-col span="10">
        <u-search :show-action="false" placeholder="日照香炉生紫烟" v-model="searchKey"></u-search>
      </u-col>
      <u-col span="1">
        <u-icon name="chat" size="24"/>
      </u-col>
      <u-col span="1">
        <u-icon name="calendar" size="24"/>
      </u-col>
    </u-row>
  </view>

</template>

<script>
export default {
  data() {
    return {
      searchKey:''
    };
  }
}
</script>

<style lang="scss">
.search-bar{
  padding: 12px 10px;
  background: #fff;
}
</style>
