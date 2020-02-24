<template>
  <!-- 排行榜 -->
  <div class="paihangbang" data-ride="carousel">
    <div class="live-rank">
      <a href="https://live.bilibili.com/650" target="_blank" class="live-rank-item" v-for="(paihang,index) in paihangs" :key="index">
        <div class="rank-face">
          <span class="number" :class="{on:paihang.first<4?true:false}">{{paihang.first}}</span>
          <img
            :src=paihang.paihangImg
            alt
          />
          <div class="txt">
            <p>{{paihang.name}}</p>
            <p class="p2">{{paihang.title}}</p>
          </div>
        </div>
        <div class="count">
          <i class="iconfont iconcc-users"></i>{{paihang.number}}
        </div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      paihangs: [
        {
          name: "一米八的坤儿",
          title: "账号双双双双双被检测了",
          number: "64.6万",
          paihangImg: require("@/images/paihang/paihang1.png"),
          first:1
        },
        {
          name: "哔哩哔哩英雄联盟赛事",
          title: "LPL百大经典战役特辑",
          number: "57.8万",
          paihangImg: require("@/images/paihang/paihang2.png"),
          first:2
        },
        {
          name: "两仪滚",
          title: "【滚 《 手 枪 皇 帝 》",
          number: "56.0万",
          paihangImg: require("@/images/paihang/paihang3.png"),
          first:3
        },
        {
          name: "OldBa1",
          title: "捡垃圾快乐",
          number: "53.7万",
          paihangImg: require("@/images/paihang/paihang4.png"),
          first:4
        },
        {
          name: "老骚豆腐",
          title: "【豆腐】迷失岛3二周目！",
          number: "52.5万",
          paihangImg: require("@/images/paihang/paihang5.png"),
          first:5
        },
        {
          name: "沉默寡言白河愁",
          title: "鸽了两年的大鱼吃小鱼主播！",
          number: "36.1万",
          paihangImg: require("@/images/paihang/paihang6.png"),
          first:6
        }
      ]
    };
  }
};
</script>

<style lang="less" scoped>
.paihangbang {
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