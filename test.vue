<template>
  <div class="content" ref="content">
    <Bottom :class="showBottom?'hasKb':'noKb'" ref="bottom"></Bottom>
  </div>
</template>

<script>
  import Bottom from '../components/updateorder/Bottom'
  export default {
    data () {
      return {
        showBottom: true,       // 底部的按钮是不是显示（处理键盘弹出的时候）
        originHeight: 0, // 开始高度
        screenHeight: 0  // 动态变化高度
      }
    },
    watch: {
      screenHeight (val) {
        this.showBottom = val < this.originHeight
      }
    },
    mounted () {
      this.originHeight = this.$refs.bottom.$el.offsetTop
      this.$nextTick(() => {
        this.screenHeight = this.$refs.bottom.$el.offsetTop
      })
      window.onresize = () => {
        return (() => {
          this.screenHeight = this.$refs.bottom.$el.offsetTop
        })()
      }
    },
    components: {
      Bottom
    }
  }
</script>

<style type="text/scss" lang="scss" scoped>
  @import "../assets/css/base";

  .content {
    overflow: hidden;
    margin-bottom: pr(60);
  }

  .hasKb {
    opacity: 0;
    pointer-events: none;
  }

  .noKb {
    opacity: 1;
    pointer-events: auto;
  }
</style>
