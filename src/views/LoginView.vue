<template>
  <div class="login_view">
    <div class="shadow"></div>
    <video muted ref="video" loop src="https://slwl-admin.itheima.net/static/media/video.3cf57b17.mp4"></video>
  </div>
</template>

<script lang='ts' setup name="Login">
import { ref, onMounted } from 'vue'
const video = ref<HTMLVideoElement | null>(null)

onMounted(() => {
  // 初始化视频播放
  video.value?.play()
})
</script>

<style lang='less' scoped>
.login_view {
  width: 100%;
  height: 100%;
  .shadow {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    opacity: .3;
    background: #1a1c41;
    z-index: 1;
  }
  video{
    width: 100%;
    height: 100%;
    object-fit: fill;
    overflow-clip-margin: content-box;
  }
  
}
</style>