<template>
  <div class="container banner_wrapper">
    <div class="extension">
      <header class="storey-title">
        <div class="l-con">
          <i class="icon"></i>
          <span class="name no-link">正在直播</span>
          <div class="text-info">
            <a href="javascript:;" target="_blank" class="text-info-link">
              <i class="iconfont iconicon-test" v-if="iconShow"></i>当前共有 19299 个在线直播
            </a>
            <a href="javascript:;" target="_blank" class="text-info-link">
              <i class="iconfont iconicon-test"></i>233秒竟然能做这些！
            </a>
          </div>
        </div>
        <div class="exchange-btn">
          <div class="btn btn-change yuanjiao">
            <i class="iconfont iconshuaxin"></i>
            换一换
          </div>
          <a href="//live.bilibili.com/" target="_blank" class="btn more yuanjiao">
            更多
            <i class="iconfont iconjiantouarrow487"></i>
          </a>
        </div>
      </header>
      <div class="ext-box">
        <div class="video-card" v-for="(storeyImg,num) in storeyImgs" :key="num">
          <div class="card-pic">
            <a href="javascript:;">
              <img class="yuanjiao" :src="storeyImg.imgUrl" />
              <div class="count" style="position:absolute;z-index:1;">
                <div class="left">
                  <i class="iconfont iconcc-users"></i>
                  <span>{{storeyImg.person}}</span>
                </div>
              </div>
            </a>
            <div class="bgcolor yuanjiao" style="height:116px;top:0;"></div>
          </div>
          <div class="title_l_wrapper">
            <img :src="storeyImg.avatar" style="width:36px;height:36px;" alt />
            <div class="title_r_wrapper">
              <a class="title">{{storeyImg.name}}</a>
              <p class="title" style="margin:4px 0;">{{storeyImg.desc}}</p>
              <p class="title ex-up">{{storeyImg.biaoti}}</p>
            </div>
          </div>

          <!-- 可显示可不显示的up -->
          <a href="javascript:;" class="ex-upzhu ex-up" v-show="iconShow">
            <i class="iconfont iconUPzhu"></i>
            11
          </a>
        </div>
      </div>
    </div>
    <div class="live-tabs">
      <!-- 导航按钮 -->
      <ul class="tab-switch">
        <div
          v-for="(tab,tabIndex) in menu"
          :key="tabIndex"
          :class="{on:(isActive==tab.value?true:false)}"
          class="tab-switch-item"
          @click="isActive=tab.value;currentComp=tab.comp"
        >{{tab.name}}</div>
      </ul>
      <!-- 需要显示的组件 -->
      <div>
        <Paihang :is="currentComp"></Paihang>
      </div>
    </div>
    <div id="elevator" class="elevator" :style="{top: activeTop}">
      <div class="mask"></div>
      <i class="ear iconfont iconbilibili-line"></i>
      <div class="list-box">
        <div>
          <div class="item sortable">直播</div>
          <div class="item sortable">动画</div>
          <div class="item sortable">番剧</div>
          <div class="item sortable">国创</div>
          <div class="item sortable">漫画</div>
          <div class="item sortable">音乐</div>
          <div class="item sortable">舞蹈</div>
          <div class="item sortable">游戏</div>
          <div class="item sortable">科技</div>
          <div class="item sortable">数码</div>
          <div class="item sortable">生活</div>
          <div class="item sortable">鬼畜</div>
          <div class="item sortable">时尚</div>
          <div class="item sortable">广告</div>
          <div class="item sortable">娱乐</div>
          <div class="item sortable">专栏</div>
          <div class="item sortable">电影</div>
          <div class="item sortable">TV剧</div>
          <div class="item sortable">影视</div>
          <div class="item sortable">纪录片</div>
        </div>
        <div class="item sort">
          <i class="iconfont iconqiehuan"></i>
        </div>
        <div class="item back-top">
          <a href="#">
            <i class="iconfont iconjiantouarrow487"></i>
          </a>
        </div>
        <div class="item back-old">
          返回
          <br />旧版
        </div>
      </div>
      <div class="bg23"></div>
    </div>
  </div>
</template>

<script>
import Paihang from "./Children/Paihang.vue";
import Tuijian from "./Children/Tuijian.vue";
import Zhubo from "./Children/Zhubo.vue";

export default {
  data() {
    return {
      iconShow: false,
      storeyImgs: [
        {
          imgUrl:
            require("@/images/storey1.png"),
          avatar:
            require("@/images/avatar1.png"),
          biaoti: "攻抗疫情",
          name: "东方网EASTDAY",
          desc: "战疫情丨陕西在行动第二十五场大型融媒体直播",
          person: "3870"
        },
        {
          imgUrl:
            require("@/images/storey2.png"),
          avatar:
            require("@/images/avatar2.png"),
          biaoti: "视频唱见",
          name: "赤瞳音乐RubyEyes",
          desc: "赤瞳音乐 | 【茧】线上音乐节",
          person: "4094"
        },
        {
          imgUrl:
            require("@/images/storey3.png"),
          avatar:
            require("@/images/avatar3.png"),
          biaoti: "视频聊天",
          name: "o我就吃一口o",
          desc: "和封面不一样",
          person: "341"
        },
        {
          imgUrl:
            require("@/images/storey4.png"),
          avatar:
            require("@/images/avatar4.png"),
          biaoti: "其他单机",
          name: "风竹教主解说",
          desc: "只会下跪の刀神！",
          person: "3.5万"
        },
        {
          imgUrl:
            require("@/images/storey5.png"),
          avatar:
            require("@/images/avatar5.png"),
          biaoti: "视频聊天",
          name: "是小阿妮呀",
          desc: "萌新第1天播",
          person: "82"
        },
        {
          imgUrl:
            require("@/images/storey6.png"),
          avatar:
            require("@/images/avatar6.png"),
          biaoti: "其他单机",
          name: "礼赞Citicav",
          desc: "【罗马2 全面战争】",
          person: "7599"
        },
        {
          imgUrl:
            require("@/images/storey7.png"),
          avatar:
            require("@/images/avatar7.png"),
          biaoti: "其他单机",
          name: "爆走短路",
          desc: "刺杀指挥官",
          person: "1986"
        },
        {
          imgUrl:
            require("@/images/storey8.png"),
          avatar:
            require("@/images/avatar8.png"),
          biaoti: "聊天电台",
          name: "糖羽儿",
          desc: "【声优】我坦白，我想骗你",
          person: "842"
        },
        {
          imgUrl:
            require("@/images/storey9.png"),
          avatar:
            require("@/images/avatar9.png"),
          biaoti: "虚拟主播",
          name: "铃音_Official",
          desc: "练琴弹唱摸鱼w",
          person: "1.7万"
        },
        {
          imgUrl:
            require("@/images/storey10.png"),
          avatar:
            require("@/images/avatar10.png"),
          name: "小可学妹",
          desc: "♥进来van♂♥",
          biaoti: "唱见电台",
          person: "2119"
        }
      ],
      currentComp: "Paihang",
      isActive: 1,
      menu: [
        {
          name: "直播排行榜",
          value: 1,
          comp: "Paihang"
        },
        {
          name: "关注的主播",
          value: 2,
          comp: "Zhubo"
        },
        {
          name: "为你推荐",
          value: 3,
          comp: "Tuijian"
        }
      ],
      activeTop: 288+'px'
    };
  },
  mounted() {
    window.addEventListener("scroll", this.hidemenu); //监听滚动事件
  },
  methods: {
    hidemenu() {
      let scrollTop =
        window.pageYOffset ||
        document.documentElement.scrollTop ||
        document.body.scrollTop;
      //当滚动超过50时，实现吸顶效果（导航高度为50）
      if (scrollTop > 288) {
        this.activeTop =10+ "px";
      } else {
        this.activeTop = 288 + "px";
      }
    }
  },
  components: {
    Paihang,
    Tuijian,
    Zhubo
  }
};
</script>

<style lang="less" scoped>
.banner_wrapper {
  height: 456px;
  margin-bottom: 40px;
  display: flex;
  justify-content: space-between;

  .extension {
    .storey-title {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 16px;
      height: 36px;
      .l-con {
        display: flex;
        justify-content: space-between;
        .icon {
          display: inline-block;
          width: 28px;
          height: 28px;
          background: url("../../images/icon-1.png") no-repeat center;
          background-size: 27.59px;
          margin-right: 6px;
          margin-top: 3px;
        }
        .name {
          font-size: 22px;
          line-height: 35px;
          margin-right: 20px;
          cursor: pointer;
          &:hover {
            color: #00a1d6;
          }
        }
        .text-info {
          i {
            color: #f0361b;
            margin-right: 3px;
            margin-left: 13px;
          }
          .text-info-link {
            line-height: 38px;
          }
        }
      }
      .exchange-btn {
        .btn-change {
          width: 70px;
          height: 26px;
          line-height: 24px;
          border: 1px solid #ccc;
          font-size: 12px;
          padding: 0;
          &:hover {
            background: #f4f4f4;
            .iconfont {
              transform: rotate(-1turn);
            }
          }
          .iconfont {
            display: inline-block;
            transition: all 0.5s;
          }
        }
        .more {
          width: 50px;
          height: 26px;
          line-height: 24px;
          padding: 0 0 0 5px;
          display: inline-block;
          border: 1px solid #ccc;
          font-size: 12px;
        }
        i {
          font-size: 12px;
        }
      }
    }
    .ext-box {
      display: flex;
      justify-content: space-between;
      width: 1070px;
      height: 404px;
      flex-wrap: wrap;
      align-content: space-between;
      .video-card {
        width: 206px;
        height: 192px;
        .card-pic {
          position: relative;
          img {
            width: 206px;
            height: 116px;
          }
          .count {
            position: absolute;
            left: 10px;
            bottom: 8px;
            .left {
              color: #fff;
              font-size: 12px;
            }
          }
        }

        .title_l_wrapper {
          display: flex;
          margin-top: 10px;
          .title_r_wrapper {
            cursor: pointer;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            overflow: hidden;
            margin-left: 16px;
          }
        }
        .title {
          // width: 206px;
          text-overflow: ellipsis;
          white-space: nowrap;
          overflow: hidden;
        }
        .ex-upzhu {
          display: inline-block;
          margin-top: 60px;
        }
      }
    }
  }

  .live-tabs {
    .tab-switch {
      display: flex;
      margin-right: 16px;
      margin-bottom: 14px;
      line-height: 36px;
      .tab-switch-item {
        margin-right: 12px;
        cursor: pointer;
        &.on {
          color: #00a1d6;
          border-bottom: 1px solid #00a1d6;
        }
      }
    }
    #carousel-example-generic {
      .carousel-inner {
        display: flex;
        .item {
          position: absolute;
          .carousel-caption {
            padding: 0;
          }
        }
      }
    }
  }
  .elevator {
    position: fixed;
    left: 50%;
    top: 10px;
    margin-left: 723px;
    z-index: 10;
    .ear {
      position: absolute;
      top: -13px;
      font-size: 44px;
      left: 5px;
      z-index: -2;
    }
    .list-box {
      padding-top: 6px;
      position: relative;
      background: #fff;
      border: 1px solid #e7e7e7;
      border-top-left-radius: 10px;
      border-top-right-radius: 10px;
      z-index: 2;
      .item {
        width: 54px;
        height: 24px;
        line-height: 24px;
        text-align: center;
        cursor: pointer;
        transition: all 0.2s;
        -ms-user-select: none;
        user-select: none;
        background: #fff;
        &.sort {
          height: 32px;
          line-height: 32px;
          position: relative;
          border-top: 1px solid #e7e7e7;
          margin-top: 5px;
          .iconqiehuan {
            display: inline-block;
            transform: rotate(90deg);
          }
        }
        &.back-top {
          position: absolute;
          left: -1px;
          bottom: -32px;
          width: 56px;
          line-height: 30px;
          height: 32px;
          border: 1px solid #e7e7e7;
          border-bottom-left-radius: 10px;
          border-bottom-right-radius: 10px;
          .iconjiantouarrow487 {
            display: inline-block;
            transform: rotate(-90deg);
          }
        }
        &.back-old {
          position: absolute;
          width: 56px;
          height: 42px;
          line-height: 16px;
          left: -1px;
          bottom: -82px;
          border-radius: 10px;
          border: 1px solid #e7e7e7;
          display: flex;
          justify-content: center;
          align-items: center;
        }
        i {
          font-size: 20px;
        }
        &:hover {
          background: #00a1d6;
          color: white;
        }
      }
    }
  }
}
</style>