<template>
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
        <div class="d-1">“罗斯福”号航母——新冠疫情下美军两难境地的象征!</div>
        <div class="d-2" :class="{zk: !showGD}">
          罗斯福号2700名士兵被允许下船隔离#【“罗斯福”号航母——新冠疫情下美军
          两难境地的象征】法新...
        </div>
        <label
          v-if="showGD === true"
          for="check"
          ref="checkIn"
          @click="handleCheckIn"
          class="check-in"
        >更多↓</label>
        <label
          v-if="showGD === false"
          for="check"
          @click="handlecheckOut"
          ref="checkOut"
          class="check-out"
        >收起↑</label>
        <div class="d-3">
          <!-- 下面一个例子 显示了 展示第一帧图片 -->
          <video
            object-fit="cover"
            src="http://wxsnsdy.tc.qq.com/105/20210/snsdyvideodownload?filekey=30280201010421301f0201690402534804102ca905ce620b1241b726bc41dcff44e00204012882540400&bizid=1023&hy=SH&fileparam=302c020101042530230204136ffd93020457e3c4ff02024ef202031e8d7f02030f42400204045a320a0201000400"
          ></video>
        </div>
        <div class="d-4">
          <div class="list">
            <img src="/static/logo.png" alt />
            <span>999</span>
          </div>
          <div class="list">
            <img src="/static/logo.png" alt />
            <span>999</span>
          </div>
          <div class="list">
            <img src="/static/logo.png" alt />
            <span>999</span>
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
        <div class="d-1">“罗斯福”号航母——新冠疫情下美军两难境地的象征!</div>
        <div class="d-2" :class="{zk: !showGD}">
          罗斯福号2700名士兵被允许下船隔离#【“罗斯福”号航母——新冠疫情下美军
          两难境地的象征】法新...
        </div>
        <label
          v-if="showGD === true"
          for="check"
          ref="checkIn"
          @click="handleCheckIn"
          class="check-in"
        >更多↓</label>
        <label
          v-if="showGD === false"
          for="check"
          @click="handlecheckOut"
          ref="checkOut"
          class="check-out"
        >收起↑</label>
        <div class="d-3">
          <!-- 这个地方是没问题的，只是微信工具显示尾空白，其实手机显示没问题 -->
          <video
            poster="https://img.yzcdn.cn/vant/cat.jpeg"
            object-fit="cover"
            src="http://wxsnsdy.tc.qq.com/105/20210/snsdyvideodownload?filekey=30280201010421301f0201690402534804102ca905ce620b1241b726bc41dcff44e00204012882540400&bizid=1023&hy=SH&fileparam=302c020101042530230204136ffd93020457e3c4ff02024ef202031e8d7f02030f42400204045a320a0201000400"
          ></video>
        </div>
        <div class="d-4">
          <div class="list">
            <img src="/static/logo.png" alt />
            <span>999</span>
          </div>
          <div class="list">
            <img src="/static/logo.png" alt />
            <span>999</span>
          </div>
          <div class="list">
            <img src="/static/logo.png" alt />
            <span>999</span>
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
      showGD: true,
    }
  },
  methods: {
    handleCheckIn () {
      this.showGD = false
      // this.setData({ showGD: true })
    },
    handlecheckOut () {
      this.showGD = true
      // this.setData({ showGD: false })
    }
  },
  components: {

  },
}

</script>
<style lang='scss' scoped>
.v-area-1 {
  color: #999999;
  font-size: 24upx;
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
      .d-1 {
        font-size: 26rpx;
        color: #000;
        margin: 20rpx 0;
      }
      .d-2 {
        max-height: 30rpx;
        overflow: hidden;
        transition: max-height 0.25s;
      }
      .zk {
        /*:checked 选择器匹配每个选中的输入元素（仅适用于单选按钮或复选框）,在选中后的样式*/
        max-height: 500px;
        /* border: 1px solid saddlebrown;*/
      }
      label {
        color: #1c7eff;
      }
      .d-3 {
        margin-top: 30rpx;
        video {
          width: 100%;
          height: 280rpx;
          object-fit: cover;
        }
      }
      .d-4 {
        display: flex;
        align-items: center;
        margin-top: 20rpx;
        text-align: center;
        .list {
          width: 33%;
          height: 40rpx;
          line-height: 40rpx;
          // border: 1px solid red;
          text-align: center;
          img {
            display: inline-block;
            width: 40rpx;
            height: 40rpx;
            object-fit: cover;
            margin-right: 10rpx;
          }
          span {
            vertical-align: 8rpx;
            color: #999;
          }
        }
      }
    }
  }
}
</style>