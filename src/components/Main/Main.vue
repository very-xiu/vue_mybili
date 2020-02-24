<template>
  <div class="container">
    <div class="banner_wrapper">
      <div class="left_banner">
        <div class="block" id="bannerId">
          <ul class="img-list">
            <li v-for="(item,index) in imgUrl" :key="index">
              <a href="javascript:;" style="position: relative;">
                <p :class="{'show':true}">
                  <span class="guanggao" :style="{'display':item.type===1?'inline-bloc':'none'}">广告</span>
                  &nbsp;{{item.title}}
                </p>
                <img :src="item.img" alt />
              </a>
            </li>
          </ul>

          <!-- 指示器 -->
          <div class="pointer">
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
            <a href="javascript:;"></a>
          </div>

          <!-- 左右箭头 -->
          <div class="prev-next" id="prevNext">
            <a href="javascript:;" class="prev" id="prevLeft"></a>
            <a href="javascript:;" class="next" id="nextRight"></a>
          </div>
        </div>
      </div>
      <div class="right_banner">
        <div
          class="img_wrapper yuanjiao"
          style="position:relative;"
          v-for="(rightImg,i) in rightImgs"
          :key="i"
        >
          <a href="javascript:;">
            <p class="right_text">{{rightImg.title}}</p>
            <img :src="rightImg.img" />
          </a>
          <div class="bgcolor t yuanjiao"></div>
        </div>
      </div>
    </div>
    <div class="banner_wrapper">
      <div class="extension">
        <header class="storey-title">
          <div class="l-con">
            <i class="iconfont iconyewutuiguang"></i>
            <span class="name no-link">推广</span>
            <div class="text-info">
              <a href="javascript:;" target="_blank" class="text-info-link">
                <i class="iconfont iconicon-test"></i>花式吃播·100种养膘指南
              </a>
              <a href="javascript:;" target="_blank" class="text-info-link">
                <i class="iconfont iconicon-test"></i>武汉加油！我们与你同在
              </a>
            </div>
          </div>
        </header>
        <div class="ext-box">
          <div class="video-card" v-for="(extBox,index) in extBoxs" :key="index">
            <div class="card-pic">
              <a href="javascript:;">
                <img class="yuanjiao" :src="extBox.img" alt />
                <div class="count" style="position:absolute;z-index:1;">
                  <div class="right">
                    <span>{{extBox.time}}</span>
                  </div>
                </div>
                <p class="title">{{extBox.title}}</p>
              </a>
              <div class="bgcolor yuanjiao" style="height:116px;top:0;"></div>
            </div>
            <a href="javascript:;" class="ex-up">
              <i class="iconfont iconUPzhu"></i>
              {{extBox.up}}
            </a>
          </div>
        </div>
      </div>
      <div class="gg-window">
        <div class="online">
          <a href="javascript:;">在线列表</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { move } from "../../js/tools.js";
export default {
  data() {
    return {
      imgUrl: [
        {
          img: require("@/images/left-banner1.jpg"),
          title: "这个世界，需要更多沙雕！",
          type: 0
        },
        {
          img: require("@/images/left-banner2.jpg"),
          title: "敖丙，申公豹限时获取！",
          type: 1
        },
        {
          img: require("@/images/left-banner3.jpg"),
          title: "新型冠状病毒肺炎实时进展",
          type: 0
        },
        {
          img: require("@/images/left-banner4.jpg"),
          title: "又一个快被吃灭绝的动物",
          type: 0
        },
        {
          img: require("@/images/left-banner5.jpg"),
          title: "伍佰早就是年轻人收割机了。",
          type: 0
        }
      ],
      pointerImg: require("@/images/icon_slide_selected@1x.png"),
      rightImgs: [
        {
          img: require("@/images/right-banner1.jpg"),
          title:
            "布洛妮娅竖起大拇指系列【动画风格渲染测试】Mellow Mellow【大神犬PV付】"
        },
        {
          img: require("@/images/right-banner2.jpg"),
          title: "【才浅制作】手工是有极限的 除非超越手工 善逸雷刃极致还原"
        },
        {
          img: require("@/images/right-banner3.jpg"),
          title:
            "【宝可梦特别篇13】16个道馆首领齐聚石英高原！最强道馆首领对战赛开赛！"
        },
        {
          img: require("@/images/right-banner4.jpg"),
          title: "这TM就是辱骂法官的下场！！！"
        },
        {
          img: require("@/images/right-banner5.jpg"),
          title:
            "大  木  桩  子  八     女孩被迫与木桩捆绑在一起！活动受限还傲娇？大木桩子8"
        },
        {
          img: require("@/images/right-banner8.jpg"),
          title:
            "【高血糖注意】不知道播什么的郡神突发线下联动【郡道美玲/神田笑一】"
        },
        {
          img: require("@/images/right-banner6.jpg"),
          title:
            "超好看的哔哩哔哩定制系统2.0版本！不是PPT！阔爱的2233娘，快来把2233娘装进电脑！【DrBlack】【定制系统系列】！"
        },
        {
          img: require("@/images/right-banner7.jpg"),
          title:
            "【游戏众生相】电竞史上最伟大的高光时刻！背水的逆转剧！Evo moment 37！"
        }
      ],
      extBoxs: [
        {
          img: require("@/images/two-banner-1.jpg"),
          title: "【声真似】DIO父子叫你起床！你还赖床吗？",
          time: "02:10",
          up: "松子洛洛"
        },
        {
          img: require("@/images/two-banner-2.jpg"),
          title:
            "B站就你敢这样弹《迪迦奥特曼》无缝衔接，钢琴裁缝？来自童年的感动",
          time: "03:10",
          up: "大头大头哥哥"
        },
        {
          img: require("@/images/two-banner-3.jpg"),
          title: "买了全国最有名的7种香肠！一口下去滋滋冒油！",
          time: "05:19",
          up: "女胖胖"
        },
        {
          img: require("@/images/two-banner-4.jpg"),
          title: "细读经典 87: 豆瓣9.0，他就是奥斯卡的最强大脑",
          time: "25:24",
          up: "电影最Top"
        },
        {
          img: require("@/images/two-banner-5.jpg"),
          title:
            "凭什么这家川菜馆能得米其林二星？我们吃了4000元得到答案【挑爷贵系列】",
          time: "21:10",
          up: "挑爷评美食"
        }
      ]
    };
  },
  mounted() {
    this.Swiper();
  },
  methods: {
    Swiper() {
      var bannerImgList = document.getElementsByClassName("img-list")[0];
      var list = bannerImgList.children;
      // console.log(bannerImgList);
      var allImg = bannerImgList.getElementsByTagName("img");
      var bannerId = document.getElementById("bannerId");
      var pointer = bannerId.getElementsByClassName("pointer")[0];
      var allA = pointer.getElementsByTagName("a");
      var prevNext = document.getElementById("prevNext");
      // 左右箭头
      var prevLeft = document.getElementById("prevLeft");
      var nextRight = document.getElementById("nextRight");
      var arrowA = prevNext.getElementsByTagName("a");
      // console.log(arrowA);
      bannerImgList.style.width = 550 * allImg.length + "px";
      var index = 0;
      // 圆点的位置
      pointer.style.left =
        bannerId.offsetWidth - pointer.offsetWidth - 23 + "px";
      allA[index].style.backgroundImage = `url(${this.pointerImg})`;
      // allA[index].style.borderColor = "rgba(0, 0, 0, .4)";

      for (var i = 0; i < allA.length; i++) {
        allA[i].num = i;
        allA[i].onclick = function() {
          clearInterval(timer);
          index = this.num;
          // bannerImgList.style.left = "-1226"*index+"px";
          setA();
          move(bannerImgList, "left", -550 * index, 100, function() {
            autoChange();
          });
        };
      }

      // 实现点击左右的按钮实现轮播
      // console.log(list);
      nextRight.onclick = clickHandle;
      prevLeft.onclick = function() {
        clearInterval(timer);
        if (index == 0) {
          index = list.length - 1;
          // console.log(index);
          bannerImgList.style.left = -index * 550 + "px";
        }
        index--;
        move(bannerImgList, "left", -550 * index, 100, function() {
          setA();
          autoChange();
        });
        // console.log(index);
      };

      autoChange();

      var timer;
      function autoChange() {
        timer = setInterval(function() {
          index++;
          index %= allImg.length;
          move(bannerImgList, "left", -550 * index, 100, function() {
            setA();
          });
        }, 5000);
      }

      function clickHandle() {
        clearInterval(timer);
        index++;
        index %= allImg.length;
        move(bannerImgList, "left", -550 * index, 70, function() {
          setA();
          autoChange();
        });
      }

      let _this = this.pointerImg;
      function setA() {
        if (index >= allImg.length - 1) {
          index = 0;
          bannerImgList.style.left = 0 + "px";
        }
        for (var i = 0; i < allA.length; i++) {
          allA[i].style.background = "";
          allA[i].style.width = "";
          allA[i].style.height = "";
        }
        allA[index].style.background = `no-repeat url(${_this})`;
        allA[index].style.width = 15 + "px";
        allA[index].style.height = 15 + "px";
      }
    }
  }
};
</script>

<style lang="less" scoped>
.container {
  .banner_wrapper {
    height: 242px;
    margin-bottom: 40px;
    display: flex;
    justify-content: space-between;
    .left_banner {
      width: 550px;
      height: 100%;

      .block {
        overflow: hidden;
        position: relative;
        height: 100%;
        border-radius: 4px;
        .img-list {
          position: absolute;
          height: 100%;
          display: flex;

          li {
            width: 550px;
            height: 100%;
            a {
              display: block;
              height: 100%;
              img {
                width: 100%;
                height: 100%;
              }
            }
          }

          .show {
            position: absolute;
            bottom: 5px;
            left: 10px;
            color: white;
            text-shadow: 0 2px 2px #000;
            .guanggao {
              display: inline-block;
              line-height: 21px;
              width: 40px;
              height: 21px;
              text-align: center;
              background: rgba(255, 255, 255, 0.5);
              border-radius: 3px;
              text-shadow: none;
              color: #000;
            }
          }
        }

        .pointer {
          position: absolute;
          right: 35px;
          bottom: 13px;
          width: 112px;

          a {
            float: left;
            width: 16px;
            height: 16px;
            border-radius: 50%;
            background-color: #fff;
            margin-left: 6px;
          }

          a:hover,
          &.active {
            border: 2px solid #fff;
            background-color: #00a1d6;
          }
        }

        .prev-next a {
          position: absolute;
          width: 41px;
          height: 69px;
          background-image: url(../../images/icon-slides.png);
          top: 0;
          bottom: 0;
          margin: auto 0;
        }
        .prev {
          left: 0;
          background-position: -84px 0;
        }

        .prev:hover {
          background-position: 0 0;
        }

        .next {
          right: 0;
          background-position: -125px 0;
        }

        .next:hover {
          background-position: -42px 0;
        }
      }
    }
    .right_banner {
      height: 100%;
      width: 854px;
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      align-content: space-between;
      .right_text {
        color: #fff;
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
        position: absolute;
        left: 50%;
        bottom: 5px;
        transform: translateX(-50%);
        width: 186px;
        z-index: 2;
      }
      .bgcolor.t {
        top: 0;
      }
    }
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
          .iconyewutuiguang {
            color: #ffd778;
            font-size: 35px;
            margin-right: 6px;
          }
          .name {
            font-size: 22px;
            line-height: 35px;
            margin-right: 20px;
          }
          .text-info {
            i {
              color: #f0361b;
              margin-right: 3px;
            }
            .text-info-link {
              line-height: 38px;
            }
          }
        }
      }
      .ext-box {
        display: flex;
        justify-content: space-between;
        width: 1070px;
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
              bottom: 6px;
              right: 5px;
              .right {
                color: #fff;
                font-size: 12px;
              }
            }
            .title {
              width: 206px;
              height: 38px;
              position: absolute;
              overflow: hidden;
              text-overflow: ellipsis;
              display: -webkit-box;
              -webkit-line-clamp: 2;
              -webkit-box-orient: vertical;
              bottom: -50px;
              padding-right: 10px;
              left: 0;
            }
          }
          .ex-up {
            display: inline-block;
            margin-top: 60px;
          }
        }
      }
    }
    .gg-window {
      .online{
        a{
          display: inline-block;
          width: 320px;
          text-align: center;
          margin-top: 3px;
          margin-bottom: 19px;
          height: 30px;
          border: 1px solid #e7e7e7;
          border-radius: 2px;
          background: #f4f4f4;
          color: #505050;
          line-height: 30px;
        }
      }
    }
  }
}
</style>

