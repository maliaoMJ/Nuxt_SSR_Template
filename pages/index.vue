<template>
  <el-container class="indexContainer">
    <el-header class="headerContainer">
      <ul class="userBox">
        <el-popover
          placement="top-start"
          title="标题"
          width="200"
          trigger="hover"
          content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
          <li
            slot="reference"
            class="userInfo">
            <img
              src="https://wx.qlogo.cn/mmopen/vi_32/qMJdqZU8suGECfBTE0082ibOLVa11iauPxQrxRfoSAYX34T17cabu9ID5zLOVVE5U3gyw0Bib6GpuzHGOVVUYfA1Q/132"
              class="avatar">
            <span class="userName">&nbsp; 明若清渊</span>
          </li>
        </el-popover>
        <li class="signOut">
          <i class="fa fa-sign-out"/>
          &nbsp;退出
        </li>
      </ul>
    </el-header>
    <el-container>
      <el-aside class="asideContainer">
        <el-row>
          <el-col :span="24">
            <el-menu
              default-active="2"
              class="el-menu-vertical-demo"
              background-color="#2e4050"
              text-color="#fff"
              active-text-color="#ffd04b"
              @open="handleOpen"
              @close="handleClose">
              <el-submenu index="1">
                <template slot="title">
                  <i class="el-icon-location"/>
                  <span>导航一</span>
                </template>
                <el-menu-item-group>
                  <template slot="title">分组一</template>
                  <el-menu-item index="1-1">选项1</el-menu-item>
                  <el-menu-item index="1-2">选项2</el-menu-item>
                </el-menu-item-group>
                <el-menu-item-group title="分组2">
                  <el-menu-item index="1-3">选项3</el-menu-item>
                </el-menu-item-group>
                <el-submenu index="1-4">
                  <template slot="title">选项4</template>
                  <el-menu-item index="1-4-1">选项1</el-menu-item>
                </el-submenu>
              </el-submenu>
              <el-menu-item index="2">
                <i class="el-icon-menu"/>
                <span slot="title">导航二</span>
              </el-menu-item>
              <el-menu-item index="3">
                <i class="el-icon-document"/>
                <span slot="title">导航三</span>
              </el-menu-item>
              <el-menu-item index="4">
                <i class="el-icon-setting"/>
                <span slot="title">导航四</span>
              </el-menu-item>
            </el-menu>
          </el-col>
        </el-row>
      </el-aside>
      <el-main>Main</el-main>
    </el-container>
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
  methods: {
    handleOpen() {
      console.log('open')
    },
    handleClose() {
      console.log('close')
    },
    signOut() {}
  }
}
</script>

<style lang="scss">
.indexContainer {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}
.headerContainer {
  background-color: #fff;
  color: #333;
  text-align: center;
  line-height: 60px;
  box-shadow: 5px 5px 20px #000;
  .userBox {
    width: 220px;
    height: 100%;
    float: right;
    display: flex;
    flex-direction: row;
    list-style-type: none;

    li {
      flex: 1;
      display: flex;
      height: 100%;
      cursor: pointer;
      &.userInfo {
        flex: 1;
        display: flex;
        justify-content: center;
        align-items: center;
        .avatar {
          width: 44px;
          height: 44px;
          border-radius: 22px;
        }
        .userName {
          color: #3a8ee6;
          font-size: 14px;
        }
      }
      &.signOut {
        flex: 1;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #6d6767;
        font-size: 13px;
      }
    }
  }
}
.el-main {
  background-color: #e9eef3;
  color: #333;
  min-height: 800px;
}
.asideContainer {
  max-width: 220px !important;
  background: #2e4050;
}
</style>
