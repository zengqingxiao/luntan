<template>
  <div style="background:#f5f5f5">
    <div class="l-1">
      <div class="L">
        <img src="../../static/logo.png" alt />
        <span>点赞</span>
      </div>
      <img class="R" src="../../static/logo.png" alt />
    </div>
    <div class="l-1">
      <div class="L">
        <img src="../../static/logo.png" alt />
        <span>点赞</span>
      </div>
      <img class="R" src="../../static/logo.png" alt />
    </div>
    <div class="l-2">
      <div class="l">
        <img src="../../static/logo.png" alt />
      </div>
      <div class="r">
        <div class="r-t">
          <div class="d-1">小师傅</div>
          <div class="d-2">04-03</div>
        </div>
        <div class="r-b">山有木兮木有枝，心悦君兮君不知</div>
      </div>
    </div>
    <div class="l-2">
      <div class="l">
        <img src="../../static/logo.png" alt />
      </div>
      <div class="r">
        <div class="r-t">
          <div class="d-1">小师傅</div>
          <div class="d-2">04-03</div>
        </div>
        <div class="r-b">山有木兮木有枝，心悦君兮君不知</div>
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
.l-1 {
  color: #666666;
  padding: 20rpx 32rpx;
  background-color: #fff;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 10rpx;
  .L {
    font-size: 30rpx;
    display: flex;
    align-items: center;
    img {
      width: 100rpx;
      height: 100rpx;
      object-fit: cover;
      border-radius: 50%;
      margin-right: 30rpx;
    }
  }
  .R {
    width: 30rpx;
    height: 30rpx;
    object-fit: cover;
  }
}
.l-2 {
  padding: 20rpx 32rpx;
  background-color: #fff;
  display: flex;
  align-items: center;
  margin-bottom: 10rpx;
  // border: 1px solid red;
  .d-1 {
    width: 50px;
    // border: 1px solid red;
    word-break: break-word;
    /* word-wrap: normal; */
  }
  .l {
    width: 100rpx;
    height: 100rpx;
    overflow: hidden;
    border-radius: 50%;
    // border: 1px solid red;
  }
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .r {
    color: #666666;
    flex: 1;
    height: 100rpx;
    // border: 1px solid red;
    padding: 0 0 0 30rpx;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    .r-t {
      display: flex;
      align-items: center;
      justify-content: space-between;
      .d-2 {
        // color:;
        font-size: 24rpx;
      }
    }
    .r-b {
      font-size: 24rpx;
    }
  }
}
</style>