<template>
  <div class="home">
    <el-container class="container">
      <el-header class="header">
        <img src="../assets/logo.png">
        <h2>电商后台管理系统</h2>
        <a href="#">退出</a>
      </el-header>
      <el-container>
        <el-aside class="aside" unique-opened>
          <el-row>
            <el-col>
              <el-menu default-active="2">
                <el-submenu index="1">
                  <template slot="title">
                    <i class="el-icon-location"></i>
                    <span>用户管理</span>
                  </template>
                  <el-menu-item-group>
                    <el-menu-item index="users">
                      <i class="el-icon-location"></i>
                      用户列表
                    </el-menu-item>
                  </el-menu-item-group>
                </el-submenu>

                <el-submenu index="2">
                  <template slot="title">
                    <i class="el-icon-location"></i>
                    <span>权限管理</span>
                  </template>
                  <el-menu-item-group>
                    <el-menu-item index="1-1">
                      <i class="el-icon-location"></i>
                      角色列表
                    </el-menu-item>
                    <el-menu-item index="1-1">
                      <i class="el-icon-location"></i>
                      权限列表
                    </el-menu-item>
                  </el-menu-item-group>
                </el-submenu>

                <el-submenu index="3">
                  <template slot="title">
                    <i class="el-icon-location"></i>
                    <span>商品管理</span>
                  </template>
                  <el-menu-item-group>
                    <el-menu-item index="1-1">
                      <i class="el-icon-location"></i>
                      商品列表
                    </el-menu-item>
                    <el-menu-item index="1-1">
                      <i class="el-icon-location"></i>
                      分类参数
                    </el-menu-item>
                    <el-menu-item index="1-1">
                      <i class="el-icon-location"></i>
                      商品参数
                    </el-menu-item>
                  </el-menu-item-group>
                </el-submenu>

                <el-submenu index="4">
                  <template slot="title">
                    <i class="el-icon-location"></i>
                    <span>订单管理</span>
                  </template>
                  <el-menu-item-group>
                    <el-menu-item index="1-1">
                      <i class="el-icon-location"></i>
                      订单列表
                    </el-menu-item>
                  </el-menu-item-group>
                </el-submenu>

                <el-submenu index="5">
                  <template slot="title">
                    <i class="el-icon-location"></i>
                    <span>数据统计</span>
                  </template>
                   <el-menu-item-group>
                    <el-menu-item index="1-1">
                      <i class="el-icon-location"></i>
                      数据列表
                    </el-menu-item>
                  </el-menu-item-group>
                </el-submenu>
              </el-menu>
            </el-col>
          </el-row>
        </el-aside>
        <el-main>
            <router-view></router-view>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {};
</script>

<style>
.home {
  height: 100%;
}
.home .container {
  height: 100%;
}
.el-header,
.el-footer {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #d3dce6;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
.home .container .header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #fff;
}
.home .container .aside {
  /* padding-right: 20px; */
  text-align: left;
  height: 100%;
}
</style>
