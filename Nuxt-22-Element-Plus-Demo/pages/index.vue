<template>
  <div class="common-layout">
    <el-container>
      <el-header>Header</el-header>
      <el-container>
        <el-aside width="200px">Aside</el-aside>
        <el-container>
          <el-main>Main</el-main>
          <el-footer>Footer</el-footer>
        </el-container>
      </el-container>
    </el-container>
  </div>
</template>

<style scoped>
.common-layout {
  display: flex;
  flex-direction: column;

  .el-header,
  .el-footer,
  .el-main,
  .el-aside {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .el-header,
  .el-footer {
    background-color: #9cb7ce;
    color: black;
    text-align: center;
  }

  .el-aside {
    background-color: #799bb9;
    color: black;
    text-align: center;
  }

  .el-main {
    background-color: aliceblue;
    color: black;
    text-align: center;
    height: 150px;
  }
}
</style>