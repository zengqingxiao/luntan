<template>
  <div class="personal-center">
    <div class="header">
      <div class="sign-in">
        <img src="../../static/logo.png" alt />
        签到
      </div>
    </div>
    <div class="content">
      <img src="../../static/logo.png" alt />
      <div class="label">
        <div class="d-1">小师傅</div>
        <div class="d-2">十夫长</div>
      </div>
      <div class="c-b">
        <div class="list A">
          <div>300</div>
          <div>我的金币</div>
        </div>
        <div class="list A">
          <div>300</div>
          <div>我的金币</div>
        </div>
        <div class="list">
          <div>300</div>
          <div>我的金币</div>
        </div>
      </div>
    </div>
    <!-- <div class="content">
      <img src="../../static/logo.png" alt />
      <div class="label">
        <div class="d-1">小师傅</div>
        <div class="d-2">十夫长</div>
      </div>
      <div class="c-b">
        <div class="list A">
          <div>300</div>
          <div>我的金币</div>
        </div>
        <div class="list A">
          <div>300</div>
          <div>我的金币</div>
        </div>
        <div class="list">
          <div>300</div>
          <div>我的金币</div>
        </div>
      </div>
    </div>-->
    <div class="b">
      <div class="b-list">
        <div class="L">
          <img src="../../static/logo.png" alt />
          <div>升级会员特权</div>
        </div>
        <img src="../../static/logo.png" alt />
      </div>
      <div class="b-list">
        <div class="L">
          <img src="../../static/logo.png" alt />
          <div>钱包</div>
        </div>
        <img src="../../static/logo.png" alt />
      </div>
      <div class="b-list">
        <div class="L">
          <img src="../../static/logo.png" alt />
          <div>隐私</div>
        </div>
        <img src="../../static/logo.png" alt />
      </div>
      <div class="b-list">
        <div class="L">
          <img src="../../static/logo.png" alt />
          <div>我的邀请</div>
        </div>
        <img src="../../static/logo.png" alt />
      </div>
      <div class="b-list">
        <div class="L">
          <img src="../../static/logo.png" alt />
          <div>收藏</div>
        </div>
        <img src="../../static/logo.png" alt />
      </div>
      <div class="b-list">
        <div class="L">
          <img src="../../static/logo.png" alt />
          <div>浏览记录</div>
        </div>
        <img src="../../static/logo.png" alt />
      </div>
      <div class="b-list">
        <div class="L">
          <img src="../../static/logo.png" alt />
          <div>意见反馈</div>
        </div>
        <img src="../../static/logo.png" alt />
      </div>
      <div class="b-list">
        <div class="L">
          <img src="../../static/logo.png" alt />
          <div>设置</div>
        </div>
        <img src="../../static/logo.png" alt />
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
  position: relative;
  z-index: 1;
  height: 150rpx;
  background-color: #fe3f46;
  padding: 0 32rpx;
  overflow: hidden;
  text-align: right;
  .sign-in {
    display: inline-block;
    position: relative;
    text-align: right;
    width: 120rpx;
    box-sizing: border-box;
    padding: 4rpx 20rpx;
    border-radius: 20rpx;
    color: #ffffff;
    font-size: 24rpx;
    background-color: rgba($color: #000000, $alpha: 0.5);

    img {
      position: absolute;
      left: 20rpx;
      top: 10rpx;
      width: 25rpx;
      height: 25rpx;
      object-fit: cover;
    }
  }
}
.content {
  height: 250rpx;
  position: relative;
  z-index: 2;
  border-radius: 12rpx;
  background-color: #fff;
  margin: 0 32rpx;
  margin-top: -75rpx;
  text-align: center;
  box-shadow: 0pt 3pt 6pt 0pt rgba(0, 0, 0, 0.16);
  padding-top: 75rpx;
  img {
    position: absolute;
    width: 150rpx;
    height: 150rpx;
    object-fit: cover;
    border-radius: 50%;
    top: -75rpx;
    left: 0;
    right: 0;
    margin: 0 auto;
  }
  .label {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 30rpx;
    .d-1 {
      font-size: 32rpx;
      color: #333;
      margin-right: 30rpx;
    }

    .d-2 {
      font-size: 20rpx;
      background-color: #bd603f;
      height: 30rpx;
      // border: 1px solid red;
      position: relative;
      padding-right: 8rpx;
      color: #fff;
      &::before {
        content: "";
        position: absolute;
        width: 0;
        top: 0;
        left: -28rpx;
        border: 15rpx solid #bd603f;
        border-color: transparent #bd603f transparent transparent;
      }
    }
  }
  .c-b {
    display: flex;
    justify-content: space-between;
    align-content: center;
    margin: 30rpx 70rpx;
    // border: 1px solid red;
    height: 100rpx;
    .list {
      position: relative;
      color: #333;
      font-size: 28rpx;
      div {
        line-height: 50rpx;
        height: 50rpx;
      }
      &.A::before {
        position: absolute;
        content: "";
        width: 0;
        height: 50%;
        border: 1px solid #cbcbcb;
        right: -50rpx;
        top: 30rpx;
      }
    }
  }
}
.b {
  margin-top: 50rpx;
}
.b-list {
  display: flex;
  padding: 0 32rpx;
  justify-content: space-between;
  align-items: center;
  // border: 1px solid red;
  margin: 30rpx 0;
  .L {
    display: flex;
    font-size: 28rpx;
    align-items: center;
    color: #333;
    img {
      width: 50rpx;
      height: 50rpx;
      object-fit: cover;
      margin-right: 30rpx;
    }
  }
  img {
    width: 40rpx;
    height: 40rpx;
    object-fit: cover;
  }
}
</style>