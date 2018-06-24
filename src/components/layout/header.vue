<template>
     <Header class="layout-header-bar" :style="{background:'#2d8cf0'}">
        <div class="layout-logo"></div>
        <Menu mode="horizontal" :theme="theme.text" active-name="1" class="headerMenu" >
            <MenuItem name="1">
                <Icon type="ios-paper"></Icon>
                内容管理
            </MenuItem>
            <MenuItem name="2">
                <Icon type="ios-people"></Icon>
                用户管理
            </MenuItem>
            <Submenu name="3">
                <template slot="title">
                    <Icon type="stats-bars"></Icon>
                    统计分析
                </template>
                <MenuGroup title="使用">
                    <MenuItem name="3-1">新增和启动</MenuItem>
                    <MenuItem name="3-2">活跃分析</MenuItem>
                    <MenuItem name="3-3">时段分析</MenuItem>
                </MenuGroup>
                <MenuGroup title="留存">
                    <MenuItem name="3-4">用户留存</MenuItem>
                    <MenuItem name="3-5">流失用户</MenuItem>
                </MenuGroup>
            </Submenu>
            <MenuItem name="4">
                <Icon type="settings"></Icon>
                综合设置
            </MenuItem>
        </Menu>
        <div class="demo-avatar" :style="{float:right}">
           <Avatar style="background-color: #87d068" icon="person" />
        </div>
       </div>
    </Header>
</template>
<script>
export default {
  data() {
    return {
      theme: {
        // text: "dark",
        // color: "#495060"
        text: "primary",
        color: "#2d8cf0"
      },
      switch1: false
    };
  }
};
</script>
<style scoped>
.headerMenu {
  margin-left: 50%;
  margin-right: 50px;
  float: left;
}
.layout-header-bar {
  height: 60px;
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.1);
  padding: 0px;
}
.layout-logo {
  width: 100px;
  height: 30px;
  background: #5b6270;
  border-radius: 3px;
  float: left;
  position: relative;
  top: 15px;
  left: 20px;
}
</style>


