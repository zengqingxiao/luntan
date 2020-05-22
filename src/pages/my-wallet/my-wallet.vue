<template>
  <div class="my-wallet">
    <div class="header"></div>
    <div class="card">
      <div class="d-1">总资产(CNY)</div>
      <div class="d-2">
        <div class="t-1">256.00</div>
        <div class="t-2">
          <div>提现</div>
          <img src="../../static/logo.png" alt />
        </div>
      </div>
      <div class="d-3">昨日收益：￥50</div>
    </div>
    <div class="returns-detailed">
      <div class="l-1">
        <div class="d-1">收益明细</div>
        <div class="d-2">查看全部</div>
      </div>
      <div class="l-2">
        <div>帖子打赏</div>
        <div class="d-2">
          <div class="t-1">帖子打赏到账</div>
          <div class="t-2">04-22 19:08</div>
        </div>
      </div>
      <div class="l-2">
        <div>帖子打赏</div>
        <div class="d-2">
          <div class="t-1">帖子打赏到账</div>
          <div class="t-2">04-22 19:08</div>
        </div>
      </div>
      <div class="l-2">
        <div>帖子打赏</div>
        <div class="d-2">
          <div class="t-1">帖子打赏到账</div>
          <div class="t-2">04-22 19:08</div>
        </div>
      </div>
      <div class="l-2">
        <div>帖子打赏</div>
        <div class="d-2">
          <div class="t-1">帖子打赏到账</div>
          <div class="t-2">04-22 19:08</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {

    }
  },
  methods: {

  },
  components: {

  },
}

</script>
<style lang='scss' scoped>
.header {
  height: 300rpx;
  background-color: #fe3f46;
}
.card {
  margin: 0 32rpx;
  height: 280rpx;
  margin-top: -200rpx;
  border-radius: 12rpx;
  background-image: linear-gradient(#d12e34, #f95c62);
  padding: 50rpx 40rpx;
  color: #fff;
  display: flex;
  // flex-wrap: wrap;
  flex-direction: column;
  justify-content: space-between;
  .d-2 {
    // border: 1px solid #000;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .t-1 {
      font-size: 60rpx;
    }
    .t-2 {
      display: flex;
      align-items: center;
      // border: 1px solid #000;
      img {
        width: 40rpx;
        height: 40rpx;
        object-fit: cover;
        margin-left: 20rpx;
      }
    }
    // font-size: ;
  }
  .d-3 {
    font-size: 28rpx;
    // margin-top: 60rpx;
  }
}
.returns-detailed {
  margin-top: 80rpx;
  border: 1px solid red;
  padding: 0 32rpx;
  .l-1 {
    display: flex;
    align-items: center;
    color: #666666;
    justify-content: space-between;
    .d-1 {
      font-size: 40rpx;
      color: #333333;
    }
    .d-2 {
      font-size: 28rpx;
    }
  }
  .l-2 {
    margin: 50rpx 30rpx;
    // border: 1px solid red;
    .d-2 {
      display: flex;
      justify-content: space-between;
      color: #666;
      font-size: 26rpx;
      height: 50rpx;
      line-height: 50rpx;
      margin-top: 15rpx;
      .t-1 {
      }
    }
  }
}
</style>