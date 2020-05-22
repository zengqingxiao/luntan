<template>
  <!-- 音乐敬拜 -->
  <div class>
    <div class="v-area-1" style="color:#999999;font-size: 24upx;">
      <div class="all-list">
        <div class="l-header">
          <div class="img">
            <img class="img-1" src="/static/logo.png" alt />
            <img class="img-2" src="/static/logo.png" alt />
          </div>
          <div class="text">
            <div class="t-t">
              <div class="t-t-l">
                <div class="name">小白</div>
                <div class="label">十夫长</div>
              </div>
              <div class="top">置顶</div>
            </div>
            <div class="t-b">
              <div class="d-1">25分钟前</div>
              <div>100Km</div>
            </div>
          </div>
        </div>
        <div class="l-foot">
          <div class="v-1">
            <img src="../../static/logo.png" alt />
            <p>XXXXXXXX</p>
          </div>
          <div class="v-2">
            <div class="list">
              <img src="../../static/logo.png" alt />
              <span>555</span>
            </div>
            <div class="list">
              <img src="../../static/logo.png" alt />
              <span>05:36</span>
            </div>
          </div>
        </div>
      </div>
      <div class="all-list">
        <div class="l-header">
          <div class="img">
            <img class="img-1" src="/static/logo.png" alt />
            <img class="img-2" src="/static/logo.png" alt />
          </div>
          <div class="text">
            <div class="t-t">
              <div class="t-t-l">
                <div class="name">小白</div>
                <div class="label">十夫长</div>
              </div>
              <div class="top">置顶</div>
            </div>
            <div class="t-b">
              <div class="d-1">25分钟前</div>
              <div>100Km</div>
            </div>
          </div>
        </div>
        <div class="l-foot">
          <div class="v-1">
            <img src="../../static/logo.png" alt />
            <p>XXXXXXXX</p>
          </div>
          <div class="v-2">
            <div class="list">
              <img src="../../static/logo.png" alt />
              <span>555</span>
            </div>
            <div class="list">
              <img src="../../static/logo.png" alt />
              <span>05:36</span>
            </div>
          </div>
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

  }
}

</script>
<style lang='scss' scoped>
.v-area-1 {
  background-color: #f5f5f5;
  .all-list {
    padding: 20rpx 32rpx;
    box-sizing: border-box;
    margin-bottom: 20rpx;
    // border: 1px solid red;
    background-color: #fff;
    .l-header {
      display: flex;
      // border: 1px solid red;
      .img {
        width: 80rpx;
        height: 80rpx;
        position: relative;
        // border-radius: 50%;
        margin-right: 20rpx;

        .img-1 {
          width: 100%;
          height: 100%;
          object-fit: cover;
          border-radius: 50%;
        }
        .img-2 {
          position: absolute;
          right: 0;
          bottom: 0;
          width: 30%;
          height: 30%;
          object-fit: cover;
        }
      }
      .text {
        flex: 1;
        .t-t {
          display: flex;
          justify-content: space-between;
          // border: 1px solid red;
          .t-t-l {
            display: flex;
            align-items: center;
            .name {
              font-size: 30rpx;
              color: #000;
              margin-right: 30rpx;
            }
            .label {
              font-size: 20rpx;
              background-color: red;
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
                border: 15rpx solid red;
                border-color: transparent red transparent transparent;
              }
            }
          }
          .top {
            border: 1px solid #999;
            border-radius: 6rpx;
            padding: 5rpx;
            font-size: 20rpx;
          }
        }
        .t-b {
          margin-top: 13rpx;
          display: flex;
          .d-1 {
            margin-right: 20rpx;
          }
        }
      }
    }
    .l-foot {
      .v-1 {
        display: flex;
        align-items: center;
        margin-left: 100rpx;
        // border: 1px solid red;
        height: 90rpx;
        background-color: #f5f5f5;
        padding: 10rpx;
        box-sizing: border-box;
        margin-top: 20rpx;
        img {
          width: 70rpx;
          height: 70rpx;
          object-fit: cover;
          margin-right: 10rpx;
        }
        p {
          // color: #999;
          color: #000;
        }
      }
      .v-2 {
        margin-top: 20rpx;
        margin-left: 100rpx;
        display: flex;
        .list {
          display: flex;
          align-items: center;
          margin-right: 25rpx;
          img {
            width: 30rpx;
            height: 30rpx;
            object-fit: cover;
            margin-right: 8rpx;
          }
        }
      }
    }
  }
}
</style>