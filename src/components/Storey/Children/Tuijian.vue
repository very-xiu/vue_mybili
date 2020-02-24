<template>
  <!-- 轮播图 -->
  <div class="bannerMe yuanjiao" style="width: 320px; height: 330px;">
    <div class="item">
      <img :src="dataList[currentIndex]" />
    </div>
    <div class="page" v-if="this.dataList.length > 1">
      <ul>
        <li
          v-for="(item,index) in dataList"
          @click="gotoPage(index)"
          :class="{'current':currentIndex == index}"
          :key="index"
          class="yuandian"
        ></li>
      </ul>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      dataList: [
        require('@/images/tuijian/tuijian1.png'),
        require('@/images/tuijian/tuijian2.png')
      ],
      currentIndex: 0, //默认显示图片
      timer: null //定时器
    };
  },
  mounted() {
    this.runInv();
  },
  methods: {
    gotoPage(index) {
      clearInterval(this.timer);
      this.currentIndex = index;
      this.runInv();
    },

    runInv() {
      this.timer = setInterval(() => {
        this.gotoPage(this.nextIndex);
      }, 4000);
    }
  },
  computed: {
    //上一张
    prevIndex() {
      if (this.currentIndex == 0) {
        return this.dataList.length - 1;
      } else {
        return this.currentIndex - 1;
      }
    },
    //下一张
    nextIndex() {
      if (this.currentIndex == this.dataList.length - 1) {
        return 0;
      } else {
        return this.currentIndex + 1;
      }
    }
  }
};
</script>

<style lang='less' scoped>
.bannerMe {
  overflow: hidden;
  position: relative;
  .page {
    position: absolute;
    bottom: 10px;
    right: 16px;
    ul {
      display: flex;
      li {
        height: 12px;
        width: 12px;
        background-color: #fff;
        border-radius: 50%;
        cursor: pointer;
        margin-right: 7px;
        &:last-child {
          margin: 0;
        }
      }
    }
  }
}
</style>