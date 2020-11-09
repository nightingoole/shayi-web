<template>
  <div>
    <section>
      <el-carousel height="850px">
        <el-carousel-item v-for="item in 4" :key="item">
          <h3 class="small">{{ item }}</h3>
        </el-carousel-item>
      </el-carousel>
    </section>
    <section class="section" />
    <section class="section" />
    <section class="section" />
  </div>
</template>

<script>
export default {
  name: 'Main',
  data() {
    return {}
  }
}
</script>

<style scoped>
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
  text-align: center;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n+1) {
  background-color: #d3dce6;
}

.section {
  width: 100%;
  height: 200px;
  background-color: #99a9bf;
}
</style>
