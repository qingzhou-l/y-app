<template>
  <view>
    <y-card>
      <u-grid
          col="5"
          :border="false"
      >
        <u-grid-item
            v-for="(baseListItem,baseListIndex) in baseList"
            :key="baseListIndex"
        >
          <u-icon
              :customStyle="{paddingTop:20+'rpx'}"
              :name="baseListItem.name"
              :size="22"
          ></u-icon>
          <text class="grid-text">{{ baseListItem.title }}</text>
        </u-grid-item>
      </u-grid>
    </y-card>
  </view>
</template>

<script>
export default {
  data() {
    return {
      baseList: [{
        name: 'photo',
        title: '图片'
      },
        {
          name: 'lock',
          title: '锁头'
        },
        {
          name: 'star',
          title: '星星'
        },{
          name: 'star',
          title: '星星'
        },{
          name: 'star',
          title: '星星'
        },{
          name: 'star',
          title: '星星'
        },
      ]
    };
  }
}
</script>

<style lang="scss">

</style>
