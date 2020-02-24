<template>
  <!-- 关注的主播 -->
  <div class="guanzhuzhubo" data-ride="carousel">
    <div class="live-rank">
      <a href="https://live.bilibili.com/4813857" target="_blank" class="live-rank-item">
        <div class="rank-face">
          <img
            :src=zhubos
            alt
          />
          <div class="txt">
            <p>老邪说电影</p>
            <p class="p2">聊聊明星素质问题</p>
          </div>
        </div>
        <div class="count">
          <i class="iconfont iconcc-users"></i>3.3万
        </div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      zhubos:require('@/images/zhubo/zhubo1.png')
        
    };
  }
};
</script>

<style lang="less" scoped>
.guanzhuzhubo {
  width: 320px;
  .live-rank .live-rank-item {
    display: flex;
    justify-content: space-between;
    margin-bottom: 22px;
    .rank-face {
      display: flex;
      align-items: center;
      .number {
        font-size: 14px;
        color: #999;
        width: 18px;
        height: 18px;
        text-align: center;
        line-height: 18px;
        background: #fff;
        border-radius: 2px;
        display: inline-block;
        margin-right: 12px;
        &.on {
          color: #fff;
          background: #00a1d6;
        }
      }
      img {
        width: 44px;
        height: 44px;
        border-radius: 44px;
        margin-right: 12px;
      }
      .txt {
        display: inline-block;
        margin-right: 10px;
        width: 158px;
        vertical-align: middle;
        p {
          width: 100%;
          white-space: nowrap;
          overflow: hidden;
          text-overflow: ellipsis;
          &:first-child {
            font-size: 14px;
            font-weight: 900;
          }
        }
        .p2 {
          color: #505050;
          line-height: 18px;
          margin-top: 2px;
        }
      }
    }
    .count {
      color: #999;
      font-size: 12px;
      display: flex;
      white-space: nowrap;
      padding-top: 4px;
      .iconfont {
        margin-right: 4px;
      }
    }
  }
}
</style>