<template>
  <!-- 发布 -->
  <div class="container content">
    <img class="img" src="../../static/logo.png" alt />
    <p>记录美好时刻</p>
    <div class="nav">
      <div class="list">
        <img src="../../static/logo.png" alt srcset />
        <p>照片</p>
      </div>
      <div class="list">
        <img src="../../static/logo.png" alt srcset />
        <p>视频</p>
      </div>
      <div class="list">
        <img src="../../static/logo.png" alt srcset />
        <p>音频</p>
      </div>
      <div class="list">
        <img src="../../static/logo.png" alt srcset />
        <p>文档</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {}
  },
  methods: {}
}
</script>

<style lang="scss" scoped>
.content {
  padding: 32rpx;
  text-align: center;
  .img {
    width: 400rpx;
    height: 400rpx;
    object-fit: cover;
    border: 1px solid red;
    margin: 100rpx 0;
  }
  .nav {
    margin-top: 100rpx;
    display: flex;
    justify-content: space-around;
    .list {
      img {
        width: 100rpx;
        height: 100rpx;
        object-fit: cover;
        border-radius: 50%;
      }
    }
  }
}
</style>