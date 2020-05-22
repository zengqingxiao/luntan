<template>
  <div class="give-a-like" style="background:'#f5f5f5">
    <div class="l-3">
      <div class="d-1">
        <img src="../../static/logo.png" alt />
      </div>
      <div class="d-2">
        <div class="t-1">小师傅</div>
        <div class="t-2">等4人赞了你的作品</div>
        <div class="t-3">04-09</div>
      </div>
      <div class="d-3">
        <img src="../../static/logo.png" alt />
      </div>
    </div>
    <div class="l-3">
      <div class="d-1">
        <img src="../../static/logo.png" alt />
      </div>
      <div class="d-2">
        <div class="t-1">小师傅</div>
        <div class="t-2">等4人赞了你的作品</div>
        <div class="t-3">04-09</div>
      </div>
      <div class="d-3">
        <img src="../../static/logo.png" alt />
      </div>
    </div>
    <div class="l-3">
      <div class="d-1">
        <img src="../../static/logo.png" alt />
      </div>
      <div class="d-2">
        <div class="t-1">小师傅</div>
        <div class="t-2">等4人赞了你的作品</div>
        <div class="t-3">04-09</div>
      </div>
      <div class="d-3">
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
.give-a-like {
  background-color: #f5f5f5;
}
.l-3 {
  color: #666;
  background-color: #fff;
  display: flex;
  margin-bottom: 10rpx;
  padding: 20rpx;
  // border: 1px solid red;
  .d-1 {
    width: 100rpx;
    height: 100rpx;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 50%;
    }
  }
  .d-2 {
    flex: 1;
    display: flex;
    padding: 0 30rpx;
    flex-direction: column;
    justify-content: space-between;
    .t-1 {
      font-size: 30rpx;
    }
    .t-2 {
      font-size: 26rpx;
    }
    .t-3 {
      font-size: 20rpx;
    }
  }
  .d-3 {
    width: 130rpx;
    height: 130rpx;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
}
</style>