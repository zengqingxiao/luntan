<template>
  <div class="daily-attendance">
    <div class="header">
      <div class="d-1">每日签到</div>
      <div class="d-2">
        <img src="../../static/logo.png" alt />
        <div @click="handleSignInShow">已签到</div>
      </div>
      <div class="d-3">已连续签到10天，继续加油！</div>
      <uni-steps
        :options="[{title: '信徒'}, {title: '十长夫'}, {title: '五十夫长'}, {title: '百夫长'}, {title: '千夫长'}, {title: '大祭司'}]"
        :active="2"
        :activeColor="'#fff'"
      ></uni-steps>
      <div class="d-4">经验值10</div>
    </div>
    <div class="calendar">
      <view>
        <uni-calendar
          :insert="true"
          :lunar="false"
          :start-date="'2019-3-2'"
          :end-date="'2019-5-20'"
          @change="change"
        />
      </view>
    </div>
    <div class="shade" v-if="signInShow" @click="handleSignInHide">
      <div class="s-c" @click.stop="handleZZZ">
        <img src="../../static/logo.png" alt />
        <div class="d-2">经验+5</div>
        <div class="d-3">签到成功</div>
        <div class="d-4">确定</div>
      </div>
    </div>
  </div>
</template>

<script>
import uniSteps from '@/components/uni-steps/uni-steps.vue'
import uniCalendar from '@/components/uni-calendar/uni-calendar.vue'
export default {
  data () {
    return {
      signInShow: false
    }
  },
  methods: {
    /**
     *  遮罩层显示
     */
    handleSignInShow () {
      this.signInShow = true
    },
    /**
     * 遮罩层隐藏
     */
    handleSignInHide () {
      this.signInShow = false
    },
    handleZZZ () {
      // console.log('里面')
    }
  },
  components: {
    uniSteps,
    uniCalendar
  },
}

</script>
<style lang='scss' scoped>
.header {
  height: 500rpx;
  background: #fe3f46;
  color: #fff;
  text-align: center;
  .d-1 {
    font-size: 36rpx;
    padding: 30rpx 0;
  }
  .d-2 {
    border: 1px solid #fff;
    width: 230rpx;
    // text-align: center;
    justify-content: center;
    display: flex;
    align-items: center;
    margin: 0 auto;
    font-size: 36rpx;
    padding: 10rpx 0;
    box-sizing: border-box;
    border-radius: 40rpx;
    img {
      width: 50rpx;
      height: 50rpx;
      object-fit: cover;
      margin-right: 15rpx;
    }
  }
  .d-3 {
    font-size: 24rpx;
    margin: 20rpx 0 50rpx;
  }
  .d-4 {
    margin: 15rpx 0;
    font-size: 26rpx;
  }
}
.calendar {
  margin: -100rpx 32rpx 0;
  border-radius: 30rpx;
  overflow: hidden;
  box-shadow: 0pt 3pt 6pt 0pt rgba(0, 0, 0, 0.2);
}
.shade {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.2);
  .s-c {
    text-align: center;
    margin: 400rpx 100rpx;
    background-color: #fff;
    height: 410rpx;
    border-radius: 30rpx;
    box-sizing: border-box;
    // padding: ;
    line-height: 60rpx;
    img {
      width: 100rpx;
      height: 100rpx;
      object-fit: cover;
      margin-top: 50rpx;
    }
    .d-2 {
      color: #999;
      font-size: 24rpx;
    }
    .d-3 {
      // margin: 30rpx;
      font-weight: bold;
    }
    .d-4 {
      width: 230rpx;
      background-color: #fe3f46;
      text-align: center;
      color: #fff;
      // margin-top: 20rpx;
      margin: 20rpx auto 0;
      border-radius: 30rpx;
    }
  }
}
</style>