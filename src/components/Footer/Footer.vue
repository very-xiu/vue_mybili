<template>
  <div class="international-footer">
    <div class="link-box b-footer-wrap">
      <div class="link-item link-a">
        <span class="bt">bilibili</span>
        <ul>
          <a target href="javascript:;">关于我们</a>
          <a target href="javascript:;">联系我们</a>
          <a target href="javascript:;">用户协议</a>
          <a target href="javascript:;">加入我们</a>
          <a target href="javascript:;">友情链接</a>
          <a target href="javascript:;">隐私政策</a>
          <a target href="javascript:;">bilibili认证</a>
          <a target href="javascript:;">Investor Relations</a>
        </ul>
      </div>
      <div class="link-item link-b">
        <span class="bt">传送门</span>
        <ul>
          <a target href="javascript:;">帮助中心</a>
          <a target href="javascript:;">高级弹幕</a>
          <a target href="javascript:;">活动专题页</a>
          <a target href="javascript:;">侵权申诉</a>
          <a target href="javascript:;">活动中心</a>
          <a target href="javascript:;">用户反馈论坛</a>
          <a target href="javascript:;">壁纸站</a>
          <a target href="javascript:;">专车号服务中心</a>
          <a target href="javascript:;">名人堂</a>
        </ul>
      </div>
      <div class="link-item link-c">
        <a href="javascript:;" target class="biliapp">
          <i class="iconfont iconxiazai"></i>
          <p>客户端下载</p>
          <div class="qrcode"></div>
        </a>
        <a href="javascript:;" target class="weibo">
          <i class="iconfont iconweibo"></i>
          <p>新浪微博</p>
          <div class="qrcode"></div>
        </a>
        <a class="weixin">
          <i class="iconfont iconweixin-copy"></i>
          <p>官方微信</p>
          <div class="qrcode"></div>
        </a>
      </div>
    </div>
    <div class="partner b-footer-wrap">
      <div class="pic-box">
        <img src="//s1.hdslb.com/bfs/seed/jinkela/footer-v2/images/partner.png" class="pic" />
        <img
          src="https://s1.hdslb.com/bfs/static/jinkela/long/images/pic962110.png"
          width="100"
          height="40"
          class="pic962110"
        />
        <a id="jvs-cert" href="javascript:;" target style="display: block; max-width: 132px;">
          <div
            id="jvs-certifyOuter"
            class="jvs-certifyOuter"
            style="width: 100%; position: relative;"
          >
            <img
              id="certify-img1"
              class="act"
              crossorigin="anonymous"
              src="data:image/png;base64,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"
              style="position: absolute; left: 0px; top: 0px; display: block; width: 100%; height: auto; opacity: 0.85; max-height: none; border: none;"
            />
            <img
              id="certify-img2"
              class
              crossorigin="anonymous"
              src="data:image/png;base64,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"
              style="position: absolute; left: 0px; top: 0px; display: block; max-height: none; width: 100%; height: auto; opacity: 0.15; border: none;"
            />
          </div>
        </a>
      </div>
      <div class="text-con">
        <p>广播电视节目制作经营许可证：（粤）字第3248号|网络文化经营许可证：粤网文【3016】2243-112号|信息网络传播视听节目许可证：0910417</p>
        <p>
          互联网ICP备案：
          <a href="javascript:;" target>粤ICP备13002172号-3</a>粤ICP证：粤B2-20100043 |违法不良信息举报邮箱：melp@bilibili.com |违法不良信息举报电话：3300211233转3 |
          <a
            href="//static.hdslb.com/images/yyzz.png"
            target
          >营业执照</a>
        </p>
        <p>
          <i class="sprite bg1"></i>
          <a href="javascript:;" target>广东互联网举报中心</a> |
          <a href="javascript:;" target>12318全国文化市场举报网站</a> |
          <i class="sprite bg2"></i>
          <a href="javascript:;" target>粤公网安备65416513210654号</a> |
          <a href="javascript:;">儿童色情信息举报专区</a>
        </p>
        <p>
          网上有害信息举报专区：
          <i class="sprite bg3"></i>
          <a href="javascript:;" target>中国互联网违法和不良信息举报中心</a>
        </p>
        <p>亲爱的市民朋友，广东警方反诈劝阻电话“786110”系专门针对避免您财产被骗受损而设，请您一旦收到来电，立即接听。</p>
        <p>公司名称：广东宽娱数码科技有限公司|公司地址：广东省梅州市梅江路485号|电话：0752-81808888</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>

<style lang='less' scoped>
.international-footer {
  font: 12px "Helvetica Neue", Helvetica, Arial, "Microsoft Yahei",
    "Hiragino Sans GB", "Heiti SC", "WenQuanYi Micro Hei", sans-serif;
  position: relative;
  margin: 0;
  padding: 0;
  background-color: #f6f9fa;
  padding: 20px 0;
  .b-footer-wrap {
    max-width: 1414px;
    min-width: 999px;
    margin: 0 auto;
  }
  .link-box {
    font-size: 14px;
    display: flex;
    justify-content: space-between;
    .link-item {
      flex: 2;
      padding-right: 40px;
      margin-right: 40px;
      border-right: 1px solid #eee;
      .bt {
        font-size: 16px;
        color: #999;
        display: block;
        height: 20px;
        margin-bottom: 20px;
      }
      &.link-c {
        flex: 1;
        padding-right: 0;
        border-right: none;
        margin-right: 0;
        width: 300px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        .biliapp {
          color: #585f69;
          &:hover .qrcode {
            display: block;
          }
          .qrcode {
            width: 97px;
            left: -15px;
            height: 97px;
            top: -101px;
            background-image: url("../../images/biliapp_qrcode.png");
          }

          .iconxiazai {
            color: #fff;
            background-color: #585f69;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            font-size: 30px;
            margin-bottom: 10px;
            &::before {
              display: inline-block;
              margin-top: 4px;
              margin-left: 1px;
            }
          }
        }
        a {
          position: relative;
          display: inline-block;
          width: 70px;
          text-align: center;
          .qrcode {
            display: none;
            position: absolute;
            top: -125px;
            left: -25px;
            width: 117px;
            height: 117px;
            background: #fff;
            border: 1px solid #eee;
            padding: 10px;
            background-repeat: no-repeat;
            background-position: center;
          }
        }
        .weibo {
          .iconfont {
            color: #fe596c;
            margin-bottom: 8px;
          }
          &:hover .qrcode {
            display: block;
          }
          .qrcode {
            width: 100px;
            left: -19px;
            height: 100px;
            top: -100px;
            background-image: url("../../images/weibo_qrcode.png");
          }
        }
        .weixin {
          .iconfont {
            color: #42c86b;
            margin-bottom: 8px;
          }
          &:hover .qrcode {
            display: block;
          }
          .qrcode {
            width: 241px;
            left: -185px;
            height: 143px;
            top: -151px;
            background-image: url("../../images/weixin_qrcode.gif");
          }
        }
        .iconfont {
          display: inline-block;
          font-size: 40px;
        }
      }
      ul {
        height: 96px;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        a {
          display: inline-block;
          margin-bottom: 10px;
          cursor: pointer;
        }
      }
    }
  }

  .partner {
    display: flex;
    padding-top: 20px;
    color: #999;
    .pic-box {
      width: 100px;
      margin-right: 20px;
      .pic {
        width: 96px;
        height: 75px;
      }
      .pic962110 {
        margin: 5px 0;
      }
    }
    p {
      margin-bottom: 8px;
      a {
        color: #999;
      }
    }
  }
}
</style>