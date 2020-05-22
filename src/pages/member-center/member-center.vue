<template>
  <div class="member-center">
    <div class="height">
      <div class="area">
        <div class="d-1">会员卡</div>
        <div class="d-2">
          <div class="t-1">将在2021-04-13到期</div>
          <div class="t-2">立即续费</div>
        </div>
      </div>
    </div>
    <div class="select">
      <div class="s-h">
        <div>会员优选</div>
        <img @click="handleShadeShow" src="../../static/logo.png" alt />
      </div>
      <div class="s-conten">
        <div class="list" :class="{this: slect === 1}" @click="handleSelect(1)">
          <div class="top">推荐</div>
          <div class="t-1">66元/年</div>
          <div class="t-2">单帖单笔≤6元</div>
          <div class="t-3">单帖总额≤200元</div>
        </div>
        <div class="list" :class="{this: slect === 2}" @click="handleSelect(2)">
          <div class="top">8.8折</div>
          <div class="t-1">66元/年</div>
          <div class="t-2">单帖单笔≤6元</div>
          <div class="t-3">单帖总额≤200元</div>
        </div>
        <div class="list" :class="{this: slect === 3}" @click="handleSelect(3)">
          <div class="top">8.8折</div>
          <div class="t-1">66元/年</div>
          <div class="t-2">单帖单笔≤6元</div>
          <div class="t-3">单帖总额≤200元</div>
        </div>
        <div class="list" :class="{this: slect === 4}" @click="handleSelect(4)">
          <div class="top">8.8折</div>
          <div class="t-1">66元/年</div>
          <div class="t-2">单帖单笔≤6元</div>
          <div class="t-3">单帖总额≤200元</div>
        </div>
      </div>
    </div>
    <div class="shade" v-if="shadeShow">
      <div class="content">
        <div class="h">
          <img @click="handleShadeHide" src="../../static/logo.png" alt />
        </div>
        <div class="c-1">会员优选</div>
        <div class="c-2">吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾</div>
        <div class="list">
          <div class="l-1">
            <div class="d-1">A会员</div>
            <div class="d-2">66元/年</div>
          </div>
          <div class="l-2">吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾</div>
        </div>
        <div class="list">
          <div class="l-1">
            <div class="d-1">A会员</div>
            <div class="d-2">66元/年</div>
          </div>
          <div class="l-2">吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾</div>
        </div>
        <div class="list">
          <div class="l-1">
            <div class="d-1">A会员</div>
            <div class="d-2">66元/年</div>
          </div>
          <div class="l-2">吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾吊车尾</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      slect: 1,
      shadeShow: true
    }
  },
  methods: {
    handleSelect (n) {
      console.log('点击了')
      this.slect = n
    },
    handleShadeShow () {
      this.shadeShow = true
    },
    handleShadeHide () {
      this.shadeShow = false
    }
  },
  components: {

  },
}

</script>
<style lang='scss' scoped>
.member-center {
  position: relative;
  .shade {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    height: 100vh;
    background-color: rgba($color: #000000, $alpha: 0.5);
    .content {
      width: 90%;
      margin: 200rpx auto;
      box-sizing: border-box;
      height: 700rpx;
      background-color: #fff;
      border-radius: 12rpx;
      padding: 20rpx 32rpx;
      .h {
        text-align: right;
        img {
          width: 40rpx;
          height: 40rpx;
          object-fit: cover;
        }
      }
      .c-1 {
        text-align: center;
        font-size: 30rpx;
        font-weight: bold;
      }
      .c-2 {
        color: royalblue;
        font-size: 24rpx;
        margin: 40rpx 0 20rpx;
      }
      .list {
        margin: 30rpx 0;
        .l-1 {
          display: flex;
          .d-1 {
            font-size: 30rpx;
            font-weight: bold;
            margin-right: 30rpx;
          }
          .d-2 {
            font-size: 30rpx;
            color: red;
          }
        }
        .l-2 {
          margin-top: 10rpx;
          font-size: #999;
          font-size: 26rpx;
        }
      }
    }
  }
  .height {
    height: 400rpx;
    background-color: #4a4747;
    overflow: hidden;
    padding: 0 32rpx;
    .area {
      margin: 80rpx auto 0;
      width: calc(100vw - 64rpx);
      box-sizing: border-box;
      border-radius: 12rpx;
      background: url("../../static/logo.png");
      height: 300rpx;
      background-size: cover;
      background-position: center;
      padding: 40rpx;

      .d-1 {
        font-size: 50rpx;
        color: #75541f;
      }
      .d-2 {
        margin-top: 60rpx;
        font-size: 24rpx;
        color: #956c2c;
        .t-1 {
        }
        .t-2 {
          padding: 5rpx 10rpx;
          border-radius: 30rpx;
          border: 1px solid #75541f;
          width: 100rpx;
          margin-top: 15rpx;
        }
      }
    }
  }
  .select {
    background-color: #fff;
    border-top-left-radius: 40rpx;
    border-top-right-radius: 40rpx;
    // height: 500rpx;
    // border: 1px solid red;
    margin-top: -40rpx;
    padding: 100rpx 32rpx 0;
    .s-h {
      font-size: 30rpx;
      display: flex;
      align-items: center;
      img {
        width: 30rpx;
        height: 30rpx;
        object-fit: cover;
        margin-left: 20rpx;
      }
    }
    .s-conten {
      margin-top: 30rpx;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      .list {
        position: relative;
        width: 200rpx;
        height: 260rpx;
        border: 1px solid #e2ba82;
        box-sizing: border-box;
        padding: 40rpx 10rpx;
        font-size: 22rpx;
        text-align: center;
        border-radius: 12rpx;
        overflow: hidden;
        margin-bottom: 30rpx;
        .t-1 {
          color: #956c2c;
          font-size: 30rpx;
          margin: 20rpx 0;
          font-weight: bold;
        }
        .t-2,
        .t-3 {
          color: #956c2c;
          height: 40rpx;
          line-height: 40rpx;
        }
        .top {
          position: absolute;
          top: 0;
          left: 0;
          width: 60rpx;
          height: 26rpx;
          line-height: 26rpx;
          color: #fff;
          text-align: center;
          font-size: 20rpx;
          background-color: #e2ba82;
        }
      }
      .this {
        background-image: linear-gradient(#e2ba82, #f4d8ac);
        .top {
          background-color: #75541f;
        }
      }
    }
  }
}
</style>