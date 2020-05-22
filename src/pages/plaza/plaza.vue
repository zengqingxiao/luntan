<template>
  <view class="index">
    <div class="content">
      <div class="card">
        <view class="h-lists" style="margin-top: 20upx;">
          <zzx-tabs
            activeColor="#000"
            :items="items"
            :current="current"
            @clickItem="onClickItem"
            ref="mytabs"
          ></zzx-tabs>
        </view>
        <view style=" margin-top: 20upx;color:#999999;font-size: 24upx;height: 260upx;">
          <view v-show="current === 0">
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
                    <div class="list">
                      <img src="/static/logo.png" alt />
                    </div>
                    <div class="list">
                      <img src="/static/logo.png" alt />
                    </div>
                    <div class="list">
                      <img src="/static/logo.png" alt />
                      <div class="shade">+1</div>
                    </div>
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
                    <div class="list">
                      <img src="/static/logo.png" alt />
                    </div>
                    <div class="list">
                      <img src="/static/logo.png" alt />
                    </div>
                    <div class="list">
                      <img src="/static/logo.png" alt />
                      <div class="shade">+1</div>
                    </div>
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
          </view>
          <view v-show="current === 1">选项卡2的内容</view>
          <view v-show="current === 2">选项卡3的内容</view>
          <view v-show="current === 3">选项卡4的内容</view>
        </view>
        <!-- <view class>
          <button type="primary" @click="setMydot">设置dot</button>
          <button type="default" @click="removeMydot">移除dot</button>
        </view>-->
      </div>
    </div>

    <!-- <image class="logo" src="/static/logo.png"></image>
		<view>
			<text class="title">{{title}}</text>
    </view>-->
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
/deep/ .zzx-bottom-line {
  background-color: #fe3f46 !important;
}
.hidden {
  display: none;
}
.header {
  background-color: #fe3f46;
  height: 90rpx;
  display: flex;
  align-items: center;
  padding: 0 32rpx;
  color: #fff;
  img {
    width: 40rpx;
    height: 40rpx;
    object-fit: cover;
    margin-right: 20rpx;
  }
  .v-1 {
    font-size: 28rpx;
    margin-right: 40rpx;
  }
  .input {
    font-size: 24rpx;
    position: relative;
    height: 50rpx;
    line-height: 50rpx;
    width: 320rpx;
    border-radius: 30rpx;
    padding-left: 100rpx;
    background-color: rgba($color: #fff, $alpha: 0.5);
    &::after {
      content: "";
      position: absolute;
      top: 0;
      left: 40rpx;
      width: 40rpx;
      height: 40rpx;
      margin-top: 5rpx;
      background: url("/static/logo.png");
      background-size: cover;
      // border: 1px solid springgreen;
    }
  }
}
.content {
  background-color: #f5f5f5;
  .h {
    background-color: #fff;
    margin-bottom: 20rpx;
  }
  .h-img {
    height: 240rpx;
    width: 100%;
    // border: 1px solid red;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
  .icon-nav {
    // border: 1px solid red;
    margin-top: 30rpx;
    display: flex;
    flex-wrap: wrap;

    .list {
      font-size: 22rpx;
      color: #333333;
      width: 20%;
      text-align: center;
      margin-bottom: 40rpx;
      img {
        width: 80rpx;
        height: 80rpx;
        object-fit: cover;
        margin-bottom: 8rpx;
      }
    }
  }
  .notice {
    display: flex;
    height: 80rpx;
    padding: 0 32rpx;
    line-height: 80rpx;
    background-color: #fff;
    align-items: center;
    margin-bottom: 20rpx;
    .L {
      position: relative;
      width: 200rpx;
      // border: 1px solid red;
      text-align: center;
      font-size: 34rpx;
      .s-2 {
        color: #fe3f46;
        margin-left: 10rpx;
      }
      &::after {
        content: "";
        position: absolute;
        height: 60%;
        width: 0;
        top: 20%;
        right: 0;
        border: 1rpx solid #999;
      }
    }
    .R {
      font-size: 26rpx;
      color: #333333;
      padding-left: 60rpx;
    }
  }
  .card {
    background-color: #fff;
    .h-lists {
      width: 450rpx;
      // border: 1px solid red;
    }
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
            display: flex;
            justify-content: space-between;
            margin-top: 30rpx;
            .list {
              position: relative;
              width: 33.33%;
              text-align: center;
              img {
                width: 180rpx;
                height: 180rpx;
                margin: auto;
                object-fit: cover;
              }
              .shade {
                position: absolute;
                width: 180rpx;
                height: 180rpx;
                line-height: 180rpx;
                top: 0;
                left: 0;
                right: 0;
                margin: 0 auto;
                font-size: 40rpx;
                background-color: rgba($color: #000000, $alpha: 0.5);
              }
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
  }
}
</style>
