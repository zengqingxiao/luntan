<template>
  <div class="feedback">
    <div class="time">
      <span>9:41</span>
    </div>
    <div class="left">
      <img src="../../static/logo.png" alt />
      <div class="content">aaaaaaaaaaaaaaaaaaa</div>
    </div>
    <div class="right">
      <div class="content">aaaaaaaaaaaaaaaaaaa</div>
      <img src="../../static/logo.png" alt />
    </div>
    <div class="footer">
      <img src="../../static/logo.png" alt />
      <img src="../../static/logo.png" alt />
      <input type="text" />
      <span>发送</span>
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
.feedback {
  padding: 60rpx 0;
  .time {
    text-align: center;
    span {
      background-color: #d6d6d6;
      color: #ffffff;
      padding: 6rpx 20rpx;
      display: inline-block;
      font-size: 26rpx;
      border-radius: 6rpx;
    }
  }
  .left {
    margin: 30rpx 32rpx;
    display: flex;
    img {
      width: 100rpx;
      height: 100rpx;
      object-fit: cover;
      border-radius: 50%;
    }
    .content {
      position: relative;
      max-width: 300rpx;
      padding: 10rpx;
      margin-left: 20rpx;
      word-break: break-word;
      box-shadow: 0pt 3pt 6pt 0pt rgba(0, 0, 0, 0.16);
      // &::after {
      //   content: "";
      //   position: absolute;
      //   width: 0;
      //   border: 20rpx;
      // }
    }
  }
  .right {
    margin: 30rpx 32rpx;
    display: flex;
    justify-content: flex-end;
    // border: 1px solid red;
    img {
      width: 100rpx;
      height: 100rpx;
      object-fit: cover;
      border-radius: 50%;
    }
    .content {
      position: relative;
      max-width: 300rpx;
      padding: 10rpx;
      margin-right: 20rpx;
      word-break: break-word;
      box-shadow: 0pt 3pt 6pt 0pt rgba(0, 0, 0, 0.16);
    }
  }
  .footer {
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    height: 100rpx;
    // border: 1px solid red;
    // width: 100vw;
    display: flex;
    padding: 0 32rpx;
    align-items: center;
    border-top: 1px solid #f6f6f6;
    img {
      width: 50rpx;
      height: 50rpx;
      object-fit: cover;
      margin-right: 32rpx;
    }
    input {
      flex: 1;
      // border: 1px solid red;
      height: 45rpx;
      line-height: 45rpx;
      background-color: #f5f5f5;
      margin: 0 20rpx;
      border-radius: 25rpx;
    }
    span {
      width: 80rpx;
      text-align: center;
      // border: 1px solid red;
      color: #999;
      font-size: 28rpx;
    }
  }
}
</style>