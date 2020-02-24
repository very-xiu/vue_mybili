<template>
  <div id="app" ref="app">
    <div class="el-container">
      <!-- 头部区域 -->
      <div class="el-header" ref="elHeader">
        <div class="top">
          <div class="bg-img"></div>
          <div class="min-header">
            <div class="min-header-content">
              <div class="nav-link">
                <ul class="nav-link-ul">
                  <li class="nav-link-item">
                    <a href="javascript:;" class="link">
                      <i class="iconfont iconbilibili-fill"></i>
                      <span>主站</span>
                    </a>
                  </li>
                  <li class="nav-link-item">
                    <a href="javascript:;" target class="link">番剧</a>
                  </li>
                  <li class="nav-link-item">
                    <span>
                      <div
                        role="tooltip"
                        id="van-popover-9606"
                        aria-hidden="true"
                        class="van-popover van-popper popover-game"
                        style="width:undefinedpx;display:none;"
                        tabindex="0"
                      >
                        <!---->
                        <iframe
                          src="https://www.bilibili.com/page-proxy/game-nav.html"
                          frameborder="0"
                          width="100%"
                          height="100%"
                        ></iframe>
                      </div>
                      <a
                        href="javascript:;"
                        target
                        class="link van-popover__reference"
                        aria-describedby="van-popover-9606"
                        tabindex="0"
                      >游戏中心</a>
                    </span>
                  </li>
                  <li class="nav-link-item">
                    <span>
                      <div
                        role="tooltip"
                        id="van-popover-8965"
                        aria-hidden="true"
                        class="van-popover van-popper popover-live"
                        style="width:undefinedpx;display:none;"
                        tabindex="0"
                      >
                        <!---->
                      </div>
                      <a
                        href="javascript:;"
                        target
                        class="link van-popover__reference"
                        aria-describedby="van-popover-8965"
                        tabindex="0"
                      >直播</a>
                    </span>
                  </li>
                  <li class="nav-link-item">
                    <a href="javascript:;" target class="link">会员购</a>
                  </li>
                  <li class="nav-link-item">
                    <span>
                      <div
                        role="tooltip"
                        id="van-popover-5063"
                        aria-hidden="true"
                        class="van-popover van-popper popover-manga"
                        style="width:undefinedpx;display:none;"
                        tabindex="0"
                      >
                        <!---->
                      </div>
                      <a
                        href="javascript:;"
                        target
                        class="link van-popover__reference"
                        aria-describedby="van-popover-5063"
                        tabindex="0"
                      >漫画</a>
                    </span>
                  </li>
                  <li class="nav-link-item">
                    <a href="javascript:;" target class="link">赛事</a>
                  </li>
                  <li class="nav-link-item">
                    <span>
                      <a
                        href="javascript:;"
                        target
                        class="link van-popover__reference"
                        aria-describedby="van-popover-9270"
                        tabindex="0"
                      >
                        <i class="iconfont iconshouji"></i>下载APP
                      </a>
                    </span>
                  </li>
                </ul>
              </div>
              <div class="nav-search-box">
                <div class="nav-search">
                  <form id="nav_searchform">
                    <input type="text" placeholder="「拔剑神曲」原唱入驻B站" class="nav-search-keyword" />
                    <div class="nav-search-btn">
                      <button type="button" class="iconfont iconsousuo nav-search-submit"></button>
                    </div>
                  </form>
                </div>
              </div>
              <div class="nav-user-center">
                <div class="user-con search-icon">
                  <a href="javascript:;" target>
                    <i class="bilifont bili-icon_dingdao_sousuo"></i>
                  </a>
                </div>
                <div class="user-con logout">
                  <div class="item">
                    <!-- 鼠标滑过登录结构样式 -->
                    <!-- <div
                        role="tooltip"
                        id="van-popover-824"
                        aria-hidden="true"
                        class="van-popover van-popper van-popper-login"
                        tabindex="0"
                        style="width: 360px; display: none;"
                      >
                        <div class="vp-container">
                          <p class="title">登录后你可以：</p>
                          <div class="img-panel">
                            <img src="//static.hdslb.com/images/danmu.png" style="left: 0px;" />
                            <img src="//static.hdslb.com/images/danmu.png" style="left: 320px;" />
                          </div>
                          <div class="btn-box">
                            <a
                              href="//passport.bilibili.com/register/phone.html"
                              class="btn reg-btn"
                            >注册</a>
                            <a href="//passport.bilibili.com/login" class="btn">登录</a>
                          </div>
                        </div>
                        <div class="lang-change">
                          <div class="lang-item">
                            <div class="lang-title">
                              <i class="lang-icon bilifont bili-icon_dingdao_yuyanshezhi"></i>
                              语言：简体中文
                            </div>
                            <i class="lang-icon-more bilifont bili-icon_caozuo_qianwang"></i>
                          </div>
                          <div class="lang-intro">
                            <ul>
                              <li class="lang-intro-item on">
                                简体中文
                                <i class="bilifont bili-icon_caozuo_xuanzhong"></i>
                              </li>
                              <li class="lang-intro-item">
                                繁体中文
                                <i class="bilifont bili-icon_caozuo_xuanzhong"></i>
                              </li>
                            </ul>
                          </div>
                        </div>
                    </div>-->
                    <div class="login-name">
                      <img src="//static.hdslb.com/images/akari.jpg" class="logout-face" />
                      <span>登录</span>
                    </div>
                  </div>
                  <div class="item">
                    <a href="//passport.bilibili.com/register/phone.html" class="txt name">注册</a>
                  </div>
                </div>
                <div>
                  <span>
                    <button type="button" class="btn btn-danger">投稿</button>
                  </span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="container el-main">
          <div class="b-wrap">
            <div class="primary-menu-itnl">
              <div id="primaryPageTab" class="page-tab report-wrap-module">
                <ul class="con">
                  <li>
                    <a href="/">
                      <div class="round">
                        <i class="iconfont iconshouye"></i>
                      </div>
                      <span>首页</span>
                    </a>
                  </li>
                  <li>
                    <a href="//t.bilibili.com" target>
                      <div class="round yel">
                        <i class="iconfont iconiconfontdongtaidianji"></i>
                        <!---->
                      </div>动态
                    </a>
                  </li>
                  <li>
                    <a href="//www.bilibili.com/ranking" target>
                      <div class="round blue">
                        <i class="iconfont iconpaihangbang"></i>
                      </div>排行榜
                    </a>
                  </li>
                </ul>
              </div>
              <span class="tab-line-itnl"></span>
              <div id="primaryChannelMenu" class="channel-menu-itnl report-wrap-module">
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-9541"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:162px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/douga/mad/" class="name">MAD·AMV</a>
                        <a href="//www.bilibili.com/v/douga/mmd/" class="name">MMD·3D</a>
                        <a href="//www.bilibili.com/v/douga/voice/" class="name">短片·手书·配音</a>
                        <a href="//www.bilibili.com/v/douga/tokusatsu/" class="name">特摄</a>
                        <a href="//www.bilibili.com/v/douga/other/" class="name">综合</a>
                      </div>
                    </div>
                  </div>
                  <div class="item van-popover__reference">
                    <a href="//www.bilibili.com/v/douga/" class="name">
                      <span>
                        动画
                        <em>999+</em>
                      </span>
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-8431"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:172px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/anime/serial/" class="name">连载动画</a>
                        <a href="//www.bilibili.com/v/anime/finish/" class="name">完结动画</a>
                        <a href="//www.bilibili.com/v/anime/information/" class="name">资讯</a>
                        <a href="//www.bilibili.com/v/anime/offical/" class="name">官方延伸</a>
                        <a href="//www.bilibili.com/anime/timeline/" class="name">新番时间表</a>
                        <a href="//www.bilibili.com/anime/index/" class="name">番剧索引</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-8431"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/anime/" class="name">
                      <span>
                        番剧
                        <em>236</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-9506"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:268px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/music/original/" class="name">原创音乐</a>
                        <a href="//www.bilibili.com/v/music/cover/" class="name">翻唱</a>
                        <a href="//www.bilibili.com/v/music/vocaloid/" class="name">VOCALOID·UTAU</a>
                        <a href="//www.bilibili.com/v/music/electronic/" class="name">电音</a>
                        <a href="//www.bilibili.com/v/music/perform/" class="name">演奏</a>
                        <a href="//www.bilibili.com/v/music/mv/" class="name">MV</a>
                        <a href="//www.bilibili.com/v/music/live/" class="name">音乐现场</a>
                        <a href="//www.bilibili.com/v/music/other/" class="name">音乐综合</a>
                        <a href="//www.bilibili.com/audio/home?musicType=music" class="name">音频</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-9506"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/music/" class="name">
                      <span>
                        音乐
                        <em>999+</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-8495"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:214px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/guochuang/chinese/" class="name">国产动画</a>
                        <a href="//www.bilibili.com/v/guochuang/original/" class="name">国产原创相关</a>
                        <a href="//www.bilibili.com/v/guochuang/puppetry/" class="name">布袋戏</a>
                        <a href="//www.bilibili.com/v/guochuang/motioncomic/" class="name">动态漫·广播剧</a>
                        <a href="//www.bilibili.com/v/guochuang/information/" class="name">资讯</a>
                        <a href="//www.bilibili.com/guochuang/timeline/" class="name">新番时间表</a>
                        <a href="//www.bilibili.com/guochuang/index/" class="name">国产动画索引</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-8495"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/guochuang/" class="name">
                      <span>
                        国创
                        <em>154</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-5602"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:172px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/dance/otaku/" class="name">宅舞</a>
                        <a href="//www.bilibili.com/v/dance/hiphop/" class="name">街舞</a>
                        <a href="//www.bilibili.com/v/dance/star/" class="name">明星舞蹈</a>
                        <a href="//www.bilibili.com/v/dance/china/" class="name">中国舞</a>
                        <a href="//www.bilibili.com/v/dance/three_d/" class="name">舞蹈综合</a>
                        <a href="//www.bilibili.com/v/dance/demo/" class="name">舞蹈教程</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-5602"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/dance/" class="name">
                      <span>
                        舞蹈
                        <em>523</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-7631"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:240px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/game/stand_alone/" class="name">单机游戏</a>
                        <a href="//www.bilibili.com/v/game/esports/" class="name">电子竞技</a>
                        <a href="//www.bilibili.com/v/game/mobile/" class="name">手机游戏</a>
                        <a href="//www.bilibili.com/v/game/online/" class="name">网络游戏</a>
                        <a href="//www.bilibili.com/v/game/board/" class="name">桌游棋牌</a>
                        <a href="//www.bilibili.com/v/game/gmv/" class="name">GMV</a>
                        <a href="//www.bilibili.com/v/game/music/" class="name">音游</a>
                        <a href="//www.bilibili.com/v/game/mugen/" class="name">Mugen</a>
                        <a href="//www.bilibili.com/v/game/match/" class="name">游戏赛事</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-7631"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/game/" class="name">
                      <span>
                        游戏
                        <em>999+</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-2002"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:172px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/technology/fun/" class="name">趣味科普人文</a>
                        <a href="//www.bilibili.com/v/technology/wild/" class="name">野生技术协会</a>
                        <a href="//www.bilibili.com/v/technology/speech_course/" class="name">演讲·公开课</a>
                        <a href="//www.bilibili.com/v/technology/military/" class="name">星海</a>
                        <a href="//www.bilibili.com/v/technology/mechanical/" class="name">机械</a>
                        <a href="//www.bilibili.com/v/technology/automobile/" class="name">汽车</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-2002"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/technology/" class="name">
                      <span>
                        科技
                        <em>999+</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-3935"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:80px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/digital/mobile/" class="name">手机平板</a>
                        <a href="//www.bilibili.com/v/digital/pc/" class="name">电脑装机</a>
                        <a href="//www.bilibili.com/v/digital/photography/" class="name">摄影摄像</a>
                        <a href="//www.bilibili.com/v/digital/intelligence_av/" class="name">影音智能</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-3935"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/digital/" class="name">
                      <span>
                        数码
                        <em>637</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-2580"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:124px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/life/funny/" class="name">搞笑</a>
                        <a href="//www.bilibili.com/v/life/daily/" class="name">日常</a>
                        <a href="//www.bilibili.com/v/life/food/" class="name">美食圈</a>
                        <a href="//www.bilibili.com/v/life/animal/" class="name">动物圈</a>
                        <a href="//www.bilibili.com/v/life/handmake/" class="name">手工</a>
                        <a href="//www.bilibili.com/v/life/painting/" class="name">绘画</a>
                        <a href="//www.bilibili.com/v/life/sports/" class="name">运动</a>
                        <a href="//www.bilibili.com/v/life/other/" class="name">其他</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-2580"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/life/" class="name">
                      <span>
                        生活
                        <em>999+</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-3882"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:118px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/kichiku/guide/" class="name">鬼畜调教</a>
                        <a href="//www.bilibili.com/v/kichiku/mad/" class="name">音MAD</a>
                        <a
                          href="//www.bilibili.com/v/kichiku/manual_vocaloid/"
                          class="name"
                        >人力VOCALOID</a>
                        <a href="//www.bilibili.com/v/kichiku/course/" class="name">教程演示</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-3882"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/kichiku/" class="name">
                      <span class="playGame">
                        单机游戏
                        <em>169</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-1841"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:124px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/fashion/makeup/" class="name">美妆</a>
                        <a href="//www.bilibili.com/v/fashion/clothing/" class="name">服饰</a>
                        <a href="//www.bilibili.com/v/fashion/aerobics/" class="name">健身</a>
                        <a href="//www.bilibili.com/v/fashion/catwalk/" class="name">T台</a>
                        <a href="//www.bilibili.com/v/fashion/trends/" class="name">风尚标</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-1841"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/fashion/" class="name">
                      <span>
                        时尚
                        <em>786</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-8831"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/ad/ad/" class="name">
                      <span>
                        广告
                        <em>164</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-3775"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:90px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/ent/variety/" class="name">综艺</a>
                        <a href="//www.bilibili.com/v/ent/star/" class="name">明星</a>
                        <a href="//www.bilibili.com/v/ent/korea/" class="name">Korea相关</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-3775"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/ent/" class="name">
                      <span>
                        娱乐
                        <em>999+</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-4060"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:84px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/v/cinephile/cinecism/" class="name">影视杂谈</a>
                        <a href="//www.bilibili.com/v/cinephile/montage/" class="name">影视剪辑</a>
                        <a href="//www.bilibili.com/v/cinephile/shortfilm/" class="name">短片</a>
                        <a href="//www.bilibili.com/v/cinephile/trailer_info/" class="name">预告·资讯</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-4060"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/cinephile/" class="name">
                      <span>
                        影视
                        <em>999+</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-5444"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:68px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item">
                        <a href="//www.bilibili.com/documentary/" class="name">纪录片</a>
                        <a href="//www.bilibili.com/movie/" class="name">电影</a>
                        <a href="//www.bilibili.com/tv/" class="name">电视剧</a>
                      </div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-5444"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/cinema/" class="name">
                      <span>
                        放映厅
                        <em>379</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-9281"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width: 0px; display: none;"
                    tabindex="0"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item"></div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-9281"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/life/funny" class="name">
                      <span>
                        搞笑
                        <em style>999+</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-1433"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    tabindex="0"
                    style="width: 0px; display: none;"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item"></div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-1433"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/life/animal" class="name">
                      <span>
                        动物圈
                        <em>999+</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-2512"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    tabindex="0"
                    style="width: 0px; display: none;"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item"></div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-2512"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/life/food" class="name">
                      <span>
                        美食圈
                        <em>999+</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-8000"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    tabindex="0"
                    style="width: 0px; display: none;"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item"></div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-8000"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/game/stand_alone" class="name">
                      <span>
                        鬼畜
                        <em>999+</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-6870"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    tabindex="0"
                    style="width: 0px; display: none;"
                  >
                    <!---->
                    <div class="sub-container">
                      <div class="sub-item"></div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-6870"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/life/daily/#/530003" class="name">
                      <span>
                        VLOG
                        <em style="display: none;">--</em>
                      </span>
                      <!---->
                    </a>
                  </div>
                </span>
              </div>
              <span class="tab-line-itnl none"></span>
              <div id="primaryFriendshipLink" class="friendship-link report-wrap-module">
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-7177"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:112px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div style="display:flex;">
                      <div class="sub-item"></div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-7177"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/read/home" target class="name">
                      <svg aria-hidden="true" class="svg-icon" />
                      <span>专栏</span>
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-9894"
                    tabindex="0"
                  >
                    <a href="//live.bilibili.com" target class="name">
                      <svg aria-hidden="true" class="svg-icon" />
                      <span>直播</span>
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-8970"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:112px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div style="display:flex;">
                      <div class="sub-item"></div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-8970"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/blackboard/x/act_list" target class="name">
                      <svg aria-hidden="true" class="svg-icon" />
                      <span>活动</span>
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-1200"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:112px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div style="display:flex;">
                      <div class="sub-item"></div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-1200"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/blackboard/topic_list.html" target class="name">
                      <svg aria-hidden="true" class="svg-icon" />
                      <span>专题</span>
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-7358"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:112px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div style="display:flex;">
                      <div class="sub-item"></div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-7358"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/blackroom/" target class="name">
                      <svg aria-hidden="true" class="svg-icon" />
                      <span>小黑屋</span>
                    </a>
                  </div>
                </span>
                <span>
                  <div
                    role="tooltip"
                    id="van-popover-3823"
                    aria-hidden="true"
                    class="van-popover van-popper van-popper-channel"
                    style="width:112px;display:none;"
                    tabindex="0"
                  >
                    <!---->
                    <div style="display:flex;">
                      <div class="sub-item"></div>
                    </div>
                  </div>
                  <div
                    class="item van-popover__reference"
                    aria-describedby="van-popover-3823"
                    tabindex="0"
                  >
                    <a href="//www.bilibili.com/v/musicplus/" target class="name">
                      <svg aria-hidden="true" class="svg-icon" />
                      <span>音乐PLUS</span>
                    </a>
                  </div>
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- 中间区域 -->
      <Main ref="main" />

      <!-- 主题内容 -->
      <Storey/>

      <div class="mascot" id="mascot" >
        <div class="ear"></div>
        <div class="body"></div>
        <a
          href="http://search.bilibili.com/all?keyword=%E7%BE%8E%E7%90%B4&amp;from_source=gif_recommend"
          target
          title="美琴"
          class="ran-gif"
        >
          <img :src="gif" style="opacity: 1;" />
        </a>
      </div>
      <a href="javascript:;" target class="contact-help">联系客服</a>

      <!-- 底部区域 -->
      <Footer id="footer"></Footer>
    </div>
  </div>
</template>

<script>
import Main from "./components/Main/Main.vue";
import Storey from "./components/Storey/Storey.vue";
import Footer from "./components/Footer/Footer.vue";
import axios from "axios";

export default {
  data() {
    return {
      imgUrl: [
        require("@/images/icon-0.png"),
        require("@/images/icon-1.png"),
        require("@/images/icon-2.png"),
        require("@/images/icon-3.png"),
        require("@/images/icon-4.png"),
        require("@/images/icon-5.png")
      ],
      gif: require("@/images/body.gif"),
      isShow: true
    };
  },
  mounted() {
    this.newIcon();
    this._scroll();
    // console.log(this.$refs.main.$el.offsetHeight);
    /* axios('http://localhost/myweb/ajax/data.json').then(result=>{
      console.log(result);
    }) */
  },
  methods: {
    newIcon() {
      $("#primaryFriendshipLink")
        .find(".svg-icon")
        .each((index, item) => {
          $(item).attr(
            "style",
            `background:url(${this.imgUrl[index]}) no-repeat`
          );
          // console.log(item);
        });
    },
    _scroll() {
      $(window).scroll(function() {
        let scrollTop = $(this).scrollTop();
        let scrollHeight = $(document).height();
        let windowHeight = $(this).height();
        let footer = $('#footer').height();
        if (scrollTop + windowHeight >= scrollHeight-footer) {
          $('#mascot').css({'display':'none'});
        }else{
          $('#mascot').fadeIn();
        }
      });
    }
  },
  computed: {},
  components: {
    Main,
    Storey,
    Footer
  }
};
</script>

<style lang="less">
#app .el-container {
  display: flex;
  flex-direction: column;
  font-size: 14px;
  .el-header {
    padding: 0;
    height: 288px;
    .top {
      position: relative;
      width: 100%;
      background: url("./images/bili-banner.png") center;
      height: 180px;

      .bg-img {
        width: 100%;
        height: 100%;
        position: absolute;
        background-image: linear-gradient(
          to bottom,
          rgba(0, 0, 0, 0.5) 1%,
          rgba(255, 255, 255, 0) 30%
        );
      }

      .min-header {
        position: absolute;
        z-index: 1;
        width: 100%;
        height: 56px;

        .min-header-content {
          display: flex;
          height: 100%;
          padding: 10px 24px;

          justify-content: space-between;

          .nav-link {
            height: 100%;
            width: 434px;
            padding: 0;
            .nav-link-ul {
              height: 100%;
              display: flex;
              & li:first-child {
                a {
                  display: flex;
                  i {
                    margin-right: 6px;
                    font-size: 18px;
                  }
                }
              }
              & li:last-child {
                span {
                  line-height: 19px;
                  a {
                    display: inline-block;
                  }
                  i {
                    font-size: 18px;
                  }
                }
              }

              line-height: 36px;
              justify-content: space-between;
              .nav-link-item {
                .link {
                  color: #fff;
                  text-shadow: 0 1px 1px rgba(0, 0, 0, 0.5);
                }
              }
            }
          }
          .nav-search-box {
            width: 500px;
            height: 36px;
            .nav-search {
              // height: 100%;
              #nav_searchform {
                position: relative;
                display: flex;
                padding: 0 38px 0 16px;
                border: 1px solid hsla(0, 0%, 100%, 0);
                border-radius: 2px;
                background-color: #fff;
                .nav-search-keyword {
                  overflow: hidden;
                  width: 100%;
                  height: 34px;
                  border: none;
                  background-color: transparent;
                  box-shadow: none;
                  color: #999;
                  font-size: 14px;
                  line-height: 34px;
                  transition: all 0.2s;
                }
                .nav-search-btn {
                  position: absolute;
                  right: -1px;
                  top: -1px;
                  padding: 0;
                  width: 48px;
                  height: 36px;
                  border: none;
                  border-radius: 2px;
                  background: #e7e7e7;
                  line-height: 26px;
                  cursor: pointer;
                  .nav-search-submit {
                    font-weight: bold;
                    position: absolute;
                    top: 8px;
                    right: 16px;
                    margin: 0;
                    padding: 0;
                    border: none;
                    background: none;
                    color: #505050;
                    font-size: 16px;
                    line-height: 20px;
                    cursor: pointer;
                    transition: all 0.2s;
                  }
                }
              }
            }
          }
          .nav-user-center {
            width: 231px;
            height: 36px;
            display: flex;
            align-items: center;
            justify-content: flex-end;
            .mini-upload {
              color: #fff;
              text-shadow: 0 1px 1px rgba(0, 0, 0, 0.3);
              width: 100px;
              height: 36px;
              text-align: center;
              margin-left: 14px;
              background: #fb7299;
              border-radius: 2px;
            }
            .user-con {
              display: flex;
              align-items: center;
              .txt.name {
                color: #fff;
                text-shadow: 0 1px 1px rgba(0, 0, 0, 0.3);
                margin-left: 12px;
              }
              .login-name {
                display: flex;
                color: #fff;
                align-items: center;
                text-shadow: 0 1px 1px rgba(0, 0, 0, 0.3);
                white-space: nowrap;
                span {
                  cursor: pointer;
                }

                .logout-face {
                  width: 32px;
                  height: 32px;
                  border-radius: 50%;
                  display: inline-block;
                  margin-right: 5px;
                  border: 1px solid silver;
                }
              }
            }
            .btn-danger {
              width: 100px;
              height: 36px;
              background-color: #fb7299;
              border: none;
              margin-left: 14px;
            }
          }
        }
      }
    }

    .el-main {
      color: #333;
      text-align: center;
      padding: 0;
      height: 108px;
      overflow: hidden;
      .b-wrap {
        height: 100%;
        .primary-menu-itnl {
          position: relative;
          height: 100%;
          display: flex;
          padding: 20px 0;
          align-items: center;
          .page-tab {
            padding-top: 3px;
            width: 174px;
            height: 68px;
            display: flex;
            .con {
              width: 100%;
              height: 100%;
              margin: 0;
              display: flex;
              li {
                cursor: pointer;
                width: 58px;
                height: 68px;
                text-align: center;
                font-size: 14px;
                white-space: nowrap;
                border: 1px solid #fff;
                border-radius: 16px;
                transition: all 0.3s;
              }
              .round {
                position: relative;
                width: 36px;
                height: 36px;
                background: #ff5c7c;
                border-radius: 36px;
                line-height: 36px;
                text-align: center;
                margin: 0 auto 4px;

                .iconfont {
                  color: #fff;
                  font-size: 20px;
                }
              }
              .round.yel {
                background: #fcba2a;
              }
              .round.blue {
                background: #00a1d6;
              }
            }
          }
          .channel-menu-itnl {
            height: 68px;
            display: flex;
            width: 932px;
            flex-wrap: wrap;
            justify-content: space-between;
            padding-top: 5px;
            span {
              display: inline-block;
              width: 87.59px;
              height: 34px;
              .item {
                text-align: left;
                .name {
                  em {
                    font-style: normal;
                    font-size: 12px;
                    display: inline-block;
                    background: #73c9e5;
                    border-radius: 2px;
                    color: #fff;
                    margin-left: 1px;
                    transform: scale(0.85);
                    width: 32px;
                    text-align: center;
                  }
                  .playGame {
                    position: relative;
                    em {
                      position: absolute;
                      right: -3px;
                      top: 2px;
                    }
                  }
                }
              }
            }
            a:hover {
              color: #73c9e5;
            }
          }
          .friendship-link {
            position: absolute;
            right: -13px;
            top: 25px;
            width: 242px;
            height: 68px;
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            align-content: flex-start;
            > span {
              width: 60px;
              display: inline-block;
            }
            > span:last-child {
              .name {
                position: relative;
                span {
                  position: absolute;
                  top: -1px;
                  right: -16px;
                }
              }
            }
            .item {
              width: 68.47px;
              height: 34px;
              .name {
                display: flex;
                width: 100%;
                height: 100%;
                .svg-icon {
                  width: 25.19px;
                  height: 25.19px;
                }
              }
            }
          }
          .tab-line-itnl {
            display: inline-block;
            height: 46px;
            border-left: 1px solid #e7e7e7;
            margin: 0 20px;
          }
        }
      }
    }
  }

  .el-footer {
    background-color: #b3c0d1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }

  .mascot {
    position: fixed;
    bottom: 10px;
    left: 40px;
    z-index: 100;
    width: 110px;
    height: 200px;
    cursor: pointer;
    transition: transform 0.6s;
    transform-origin: left bottom;
    .ear {
      height: 26px;
      background-image: url("images/ear.png");
    }
    .body {
      position: relative;
      height: 174px;
      background-image: url("images/body.png");
    }
    .ear,
    .body {
      width: 110px;
      background-repeat: no-repeat;
      background-size: cover;
    }
    .ran-gif {
      position: absolute;
      width: 72px;
      height: 42px;
      left: 19px;
      top: 44px;
      text-align: center;
      border-radius: 6px;
      overflow: hidden;
      img {
        width: 100%;
        transition: opacity 0.5s;
      }
    }
  }
  .contact-help {
    position: fixed;
    z-index: 101;
    left: 0;
    top: calc(50% + 50px);
    margin-top: -36px;
    width: 28px;
    height: 72px;
    transition: all 0.3s;
    font-size: 12px;
    color: #505050;
    background: #fff;
    border: 1px solid #e7e7e7;
    box-shadow: 0 6px 10px 0 #e7e7e7;
    border-radius: 0 2px 2px 0;
    padding: 8px 7px;
    line-height: 14px;
    &:hover {
      background: #f4f4f4;
      color: #505050;
    }
  }
}
</style>
