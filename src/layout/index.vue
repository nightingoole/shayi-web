<template>
  <div>
    <el-container>
      <el-header>
        <el-menu
          :default-active="activeIndex2"
          mode="horizontal"
          background-color="#545c64"
          text-color="#fff"
          router
          active-text-color="#ffd04b"
          @select="handleSelect"
        >
          <el-menu-item index="1">处理中心</el-menu-item>
          <el-submenu index="2">
            <template slot="title">我的工作台</template>
            <el-menu-item index="2-1">选项1</el-menu-item>
            <el-menu-item index="2-2">选项2</el-menu-item>
            <el-menu-item index="2-3">选项3</el-menu-item>
            <el-submenu index="2-4">
              <template slot="title">选项4</template>
              <el-menu-item index="2-4-1">选项1</el-menu-item>
              <el-menu-item index="2-4-2">选项2</el-menu-item>
              <el-menu-item index="2-4-3">选项3</el-menu-item>
            </el-submenu>
          </el-submenu>
          <el-menu-item index="3" disabled>消息中心</el-menu-item>
          <el-menu-item index="4"><a href="https://www.ele.me" target="_blank">订单管理</a></el-menu-item>
        </el-menu>
      </el-header>
      <el-main>
        <router-view/>
      </el-main>
    </el-container>
  </div>
</template>

<script>
export default {
  name: 'Layout',
  data() {
    return {
      activeIndex: '1',
      activeIndex2: '1',
      pageYOffset: 0
    }
  },
  computed: {
    isNavbarFixed() {
      return this.pageYOffset >= 60 ? 'position: fixed; top: 0; width: 100%; z-index: 1000;' : ''
    }
  },
  methods: {
    handleSelect(key, keyPath) {
      // console.log(key, keyPath)
    }
  }
}
</script>

<style lang="scss" scoped>
.el-header {
  padding: 0;
  background-color: rgba(84, 92, 100, .5);
}

.el-menu-item {
  background-color: rgba(84, 92, 100, .5);
}

.el-main {
  padding: 0;
}
</style>
