<template>
  <div class="publish-content">
    <input class="input-1" type="text" placeholder="标题（6-30字之间）" />
    <textarea class="input-2" placeholder="请输入内容......"></textarea>
    <div class="bet">
      <div class="t-1">是否支持打赏</div>
      <switch checked @change="switch1Change" />
      <img class="t-2" src="../../static/logo.png" alt />
    </div>
    <div class="upload">
      <easy-upload :dataList="imageList" :types="category" :uploadCount="6"></easy-upload>
    </div>
  </div>
</template>

<script>
import easyUpload from '@/components/easy-upload/easy-upload.vue'
export default {
  data () {
    return {
      imageList: [],
      category: 'image'
    }
  },
  methods: {

  },
  components: {
    easyUpload
  },
}

</script>
<style lang='scss' scoped>
.publish-content {
  color: #999;
}
.input-1 {
  padding: 20rpx 32rpx;
  height: 50rpx;
  line-height: 50rpx;
  border-bottom: 1rpx solid #f5f5f5;
}
.input-2 {
  padding: 20rpx 32rpx;
  height: 200rpx;
  width: 100%;
  box-sizing: border-box;
  object-fit: cover;
  border-bottom: 1rpx solid #f5f5f5;
}
.bet {
  margin: 0 32rpx;
  display: flex;
  align-items: center;
  font-size: 30rpx;
  img {
    width: 30rpx;
    height: 30rpx;
  }
  .t-1,
  .t-2 {
    margin: 0 10rpx;
  }
}
.upload {
  margin: 20rpx 32rpx;
}
</style>