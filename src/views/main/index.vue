<template>
  <div>
    <section>
      <el-carousel height="850px">
        <el-carousel-item
          v-for="(item, idx) in banners"
          :key="item"
          :style="'background: url(' + item + ') center no-repeat; background-size: 100% 100%;'"
        >
          <h3 class="main-title">主标题 {{ idx }}</h3>
          <h5 class="mini-title">副标题 {{ idx }}</h5>
        </el-carousel-item>
      </el-carousel>
    </section>
    <section class="section">
      <div class="section-container section-introduce">
        <h3 class="section-title">K-CLASS 介绍</h3>
        <div class="hr">
          <hr>
          <svg-icon icon-class="section-document" />
          <hr>
        </div>
        <div class="introduce">
          <p>kclass是一个专业的语言学习平台，在这里，我们提供世界各地的语言教师</p>
          <p>通过网络授课，让您无国界的和当地人沟通</p>
        </div>
        <div class="introduce-illustration center">
          <svg-icon class="introduce-svg" icon-class="Proxy" />
        </div>
      </div>
    </section>
    <section class="section section-function">
      <div class="section-container section-introduce">
        <h3 class="section-title">服务 Service</h3>
        <div class="hr">
          <hr>
          <svg-icon icon-class="section-chat" />
          <hr>
        </div>
        <div class="introduce">
          <p>kclass是一个专业的语言学习平台，在这里，我们提供世界各地的语言教师</p>
          <p>通过网络授课，让您无国界的和当地人沟通</p>
        </div>
        <div class="introduce-illustration service">
          <el-row style="margin-bottom: 50px">
            <el-col :lg="8" :md="12" :sm="24" class="service-item center">
              <svg-icon class="service-flag" icon-class="flag-china" />
              <div class="service-desc">
                <span class="service-desc-title">中文课程</span>
                <span class="service-desc-content">中文口语 | 少儿中文 | HSK考试</span>
              </div>
            </el-col>
            <el-col :lg="8" :md="12" :sm="24" class="service-item center">
              <svg-icon class="service-flag" icon-class="flag-south-corea" />
              <div class="service-desc">
                <span class="service-desc-title">韩文课程</span>
                <span class="service-desc-content">topik考试 | 韩语口语 | 韩国入学商谈</span>
              </div>
            </el-col>
            <el-col :lg="8" :md="12" :sm="24" class="service-item center">
              <svg-icon class="service-flag" icon-class="flag-japan" />
              <div class="service-desc">
                <span class="service-desc-title">日文课程</span>
                <span class="service-desc-content">中文口语 | 少儿中文 | HSK考试</span>
              </div>
            </el-col>
          </el-row>
          <el-row>
            <el-col :lg="8" :md="12" :sm="24" class="service-item center">
              <svg-icon class="service-flag" icon-class="flag-united-states" />
              <div class="service-desc">
                <span class="service-desc-title">英语课程</span>
                <span class="service-desc-content">中文口语 | 少儿中文 | HSK考试</span>
              </div>
            </el-col>
            <el-col :lg="8" :md="12" :sm="24" class="service-item center">
              <svg-icon class="service-flag" icon-class="flag-russia" />
              <div class="service-desc">
                <span class="service-desc-title">俄语课程</span>
                <span class="service-desc-content">中文口语 | 少儿中文 | HSK考试</span>
              </div>
            </el-col>
            <el-col :lg="8" :md="12" :sm="24" class="service-item center">
              <svg-icon class="service-flag" icon-class="flag-france" />
              <div class="service-desc">
                <span class="service-desc-title">法语课程</span>
                <span class="service-desc-content">中文口语 | 少儿中文 | HSK考试</span>
              </div>
            </el-col>
          </el-row>
        </div>
      </div>
    </section>
    <section class="section section-about">
      <div class="section-container section-introduce">
        <h3 class="section-title">关于公司 About</h3>
        <div class="hr">
          <hr>
          <svg-icon icon-class="section-star" />
          <hr>
        </div>
        <div class="about" style="z-index: 1;">
          <div class="about-p">当我在学习韩语教育硕士课程的时候，我发现目前的韩语教育方法其实有很多的不足，并且我的学生都告诉我，
            他们很想在最开始学习语言的时候，就能受到正确的发音方法，表达方法等。这就是kclass的开始。</div>
          <div class="about-p">Kclass是一个第二外语的网络学习平台，在这里可以以非常优惠的课外费用找到优秀的语言教师，与此同时，
            我们还专注于向更多的学生分享留学经验，分享留学生活。kclass将立志成为您语言学习路上的好伙伴。</div>
        </div>
        <div class="introduce-illustration" style="display: flex;align-items: center; justify-content: flex-end; height: 0;">
          <svg-icon class="about-svg" icon-class="About" />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Main',
  data() {
    return {
      banners: []
    }
  },
  created() {
    this.initBanner()
  },
  methods: {
    initBanner() {
      const banner1 = require('../../assets/banner/banner1.jpg')
      const banner2 = require('../../assets/banner/banner2.jpg')
      const banner3 = require('../../assets/banner/banner3.jpg')
      const banner4 = require('../../assets/banner/banner4.jpg')
      this.banners.push(banner1)
      this.banners.push(banner2)
      this.banners.push(banner3)
      this.banners.push(banner4)
    }
  }
}
</script>

<style lang="scss" scoped>
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n+1) {
  background-color: #d3dce6;
}

.about {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;

  &-p {
    width: 350px;
    line-height: 175%;
    margin: 45px 25px;
  }

  &-svg {
    font-size: 800px;
    margin-right: -200px;
    margin-bottom: 200px;
  }
}

.service {
  padding: 0 200px;
  margin-top: 45px !important;
  margin-bottom: 100px;

  &-item {
    margin-bottom: 50px;
  }

  &-flag {
    font-size: 64px;
  }

  &-desc {
    margin-left: 10px;
    height: 64px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-between;

    &-title {
      font-weight: bold;
      font-size: 24px;
    }

    &-content {
      width: 200px;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }
  }
}

.section {
  width: 100%;

  &-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
  }

  &-title {
    font-size: 36px;
  }

  &-introduce {
    padding-top: 50px;
    overflow: hidden;
  }

  &-function {
  }

  &-about {
  }

}

.hr {
  width: 600px;
  height: 50px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}

.center {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}

.hr hr {
  width: 200px;
  height: 1px;
  background-color: #aaa;
  border: 0;
}

.hr svg {
  font-size: 36px;
}

.introduce {
  height: 100px;
  text-align: center;
  margin-top: 20px;

  &-illustration {
    width: 100%;
    height: 200px;
    margin-top: 150px;
  }

  &-svg {
    font-size: 800px;
  }

}

.section:nth-child(2n) {
  background-color: #ddd;
}

.section:nth-child(2n+1) {
  background-color: #eee;
}
</style>
