<template>
  <view class="side-menu">
    <ul>
      <li @click="changeCurrentKey(item.key)" v-for="item in menus" :key="item.label"
          :class="['side-menu-item',currentKey === item.key ?'side-menu-item-active':'']">
        {{ item.label }}
      </li>
    </ul>
  </view>
</template>

<script>
export default {
  props: {
    menus: {
      type: Array,
      required: true
    },
    defaultKey: {
      type: String
    }
  },
  data() {
    return {
      currentKey: this.defaultKey
    };
  },
  computed: {},
  methods: {
    changeCurrentKey(key) {
      this.currentKey = key
    }
  },
}
</script>

<style lang="scss">
.side-menu {
  position: fixed;
  left: 0;
  padding: 12px 0;
  min-width: 90px;
  min-height: 100%;
  background: rgb(233, 234, 238);

  &-item {
    padding: 10px;
    text-align: center;
    border-radius: 10px 0 0 10px;
    transition: background-color ease-in-out .25s;
  }
}

.side-menu-item-active {
  background: #fff;
  color: blueviolet;
}
</style>
