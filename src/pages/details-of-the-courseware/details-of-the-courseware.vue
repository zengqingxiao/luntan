<template>
  <!-- 课件详情 -->
  <view class="index">
    <div class="v-area-1">
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
            <div class="btn">下载文档</div>
          </div>
          <!-- <div class="d-4">
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
          </div>-->
        </div>
      </div>
      <div class="comment">
        <div class="list">
          <div class="l-t">
            <div class="d-1">
              <img src="../../static/logo.png" alt />
              <span>小白</span>
            </div>
            <div class="d-2">
              <img src="../../static/logo.png" alt />
              <span>255</span>
            </div>
          </div>
          <div class="l-2">严防严控病例输入，绝不能有所懈怠</div>
          <div class="l-3">
            <div class="L">
              <div class="d-1">1小时前·回复</div>
              <div class="d-2">22回复</div>
            </div>
            <div class="R">
              <img src="../../static/logo.png" alt />
            </div>
          </div>
        </div>
        <div class="list">
          <div class="l-t">
            <div class="d-1">
              <img src="../../static/logo.png" alt />
              <span>小白</span>
            </div>
            <div class="d-2">
              <img src="../../static/logo.png" alt />
              <span>255</span>
            </div>
          </div>
          <div class="l-2">严防严控病例输入，绝不能有所懈怠</div>
          <div class="l-3">
            <div class="L">
              <div class="d-1">1小时前·回复</div>
              <div class="d-2">22回复</div>
            </div>
            <div class="R">
              <img src="../../static/logo.png" alt />
            </div>
          </div>
        </div>
        <div class="list">
          <div class="l-t">
            <div class="d-1">
              <img src="../../static/logo.png" alt />
              <span>小白</span>
            </div>
            <div class="d-2">
              <img src="../../static/logo.png" alt />
              <span>255</span>
            </div>
          </div>
          <div class="l-2">严防严控病例输入，绝不能有所懈怠</div>
          <div class="l-3">
            <div class="L">
              <div class="d-1">1小时前·回复</div>
              <div class="d-2">22回复</div>
            </div>
            <div class="R">
              <img src="../../static/logo.png" alt />
            </div>
          </div>
        </div>
        <div class="list">
          <div class="l-t">
            <div class="d-1">
              <img src="../../static/logo.png" alt />
              <span>小白</span>
            </div>
            <div class="d-2">
              <img src="../../static/logo.png" alt />
              <span>255</span>
            </div>
          </div>
          <div class="l-2">严防严控病例输入，绝不能有所懈怠</div>
          <div class="l-3">
            <div class="L">
              <div class="d-1">1小时前·回复</div>
              <div class="d-2">22回复</div>
            </div>
            <div class="R">
              <img src="../../static/logo.png" alt />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="l-footer">
      <div class="d-1">
        <input class="commentary" value="写评语" type="text" />
        <img src="../../static/logo.png" alt />
      </div>
      <div class="d-2">
        <div class="list">
          <img src="../../static/logo.png" alt />
        </div>
        <div class="list">
          <img src="../../static/logo.png" alt />
        </div>
        <div class="list">
          <img src="../../static/logo.png" alt />
        </div>
        <div class="list">
          <img src="../../static/logo.png" alt />
        </div>
        <div class="list">
          <img src="../../static/logo.png" alt />
        </div>
      </div>
    </div>
  </view>
</template>

<script>
import zzxTabs from "@/components/zzx-tabs/zzx-tabs.vue"
export default {
  components: {
    zzxTabs
  },
  data () {
    return {
      showGD: true,
      title: 'Hello',
      items: ['推荐', '最新', '最热', '最近'],
      current: 0
    }
  },
  onLoad () {

  },
  methods: {
    onClickItem (e) {
      if (this.current !== e.currentIndex) {
        this.current = e.currentIndex;
      }
    },
    setMydot () {
      this.$refs.mytabs.setDot(0)
    },
    removeMydot () {
      this.$refs.mytabs.removeDot(0);
    },
    handleCheckIn () {
      this.showGD = false
      // this.setData({ showGD: true })
    },
    handlecheckOut () {
      this.showGD = true
      // this.setData({ showGD: false })
    }
  }
}
</script>

<style lang="scss" scoped>
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
        // height: 200rpx;
        .btn {
          background-color: #fe3f46;
          width: 150rpx;
          text-align: center;
          font-size: 30rpx;
          color: #fff;
          padding: 20rpx 80rpx;
          border-radius: 12rpx;
          margin: 100rpx auto 30rpx;
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
  .comment {
    width: 100%;
    // border: 1px solid red;
    .list {
      background-color: #fff;
      padding: 32rpx;
      margin-bottom: 10rpx;
      // border: 1px solid red;
      .l-t {
        display: flex;
        justify-content: space-between;
        align-items: center;
        .d-1 {
          display: flex;
          align-items: center;
          font-size: 28rpx;
          color: #000;
          img {
            width: 80rpx;
            height: 80rpx;
            object-fit: cover;
            border-radius: 50%;
            margin-right: 20rpx;
          }
        }
        .d-2 {
          display: flex;
          align-items: center;
          img {
            width: 30rpx;
            height: 30rpx;
            object-fit: cover;
            margin-right: 10rpx;
          }
        }
      }
      .l-2 {
        margin-left: 100rpx;
        color: #333;
      }
      .l-3 {
        margin-left: 100rpx;
        margin-top: 10rpx;
        display: flex;
        justify-content: space-between;
        .L {
          display: flex;
          .d-1 {
            margin-right: 10rpx;
          }
          .d-2 {
            font-size: 20rpx;
            // color: ;
            padding: 2rpx 15rpx;
            background-color: #dddddd;
            border-radius: 20rpx;
          }
        }
        .R {
          img {
            width: 30rpx;
            height: 30rpx;
            object-fit: cover;
          }
        }
      }
    }
  }
}

.l-footer {
  background-color: #fff;
  display: flex;
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100vw;
  box-sizing: border-box;
  height: 80rpx;
  // border: 1px solid red;
  padding: 15rpx 50rpx;
  .d-1 {
    // border: 1px solid red;
    width: 220rpx;
    position: relative;
    .commentary {
      width: 220rpx;
      // border: 1px solid red;
      padding-left: 80rpx;
      font-size: 24rpx;
      color: #999;
      box-sizing: border-box;
      border-radius: 80rpx;
      background-color: #f6f6f6;
    }
    img {
      position: absolute;
      width: 30rpx;
      height: 30rpx;
      object-fit: cover;
      left: 30rpx;
      top: 7rpx;
    }
  }
  .d-2 {
    flex: 1;
    margin-left: 40rpx;
    // border: 1px solid red;
    display: flex;
    align-items: center;
    justify-content: space-between;
    .list {
      width: 40rpx;
      height: 40rpx;
      position: relative;
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
      &::before {
        content: "";
        position: absolute;
        width: 15rpx;
        height: 15rpx;
        border-radius: 50%;
        right: -3rpx;
        top: -3rpx;
        background-color: red;
      }
    }
  }
}
</style>
