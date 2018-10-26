<template>
  <el-container>
    <el-header>Header</el-header>
    <el-main>Main</el-main>
  </el-container>
</template>

<script>
const HomeKey = 'Home'
export default {
  components: {},
  created: function() {
    // 获取state
    // console.log(this.$store.state.modules[HomeKey].name)
  },
  methods: {}
}
</script>

<style lang="scss">
.el-header {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  height: 600px;
}
</style>
