<!--
 * @Description: 左侧文件搜索组件
 * @Author: sufen
 * @Date: 2020-05-20 16:08:49
 * @LastEditTime: 2020-06-14 10:44:55
 * @LastEditors: sufen
 -->
<template>
  <div class="search-container">
    <!-- <el-input placeholder="请输入内容" v-bind="$attrs" v-on="$listeners">
      <el-button slot="append" icon="el-icon-search" @click.native="onSearch()" />
    </el-input> -->

    <el-button  icon="el-icon-document-add" @click.native="createFile()" type="primary" ></el-button>
    <!-- <el-dropdown-item divided @click.native="importFile()">导入文件</el-dropdown-item> -->

  </div>
</template>

<script>
// TODO:1. 加入文件夹功能
// TODO:2. 加入文件拖拽功能
export default {
  name: 'FileManager',
  methods: {
    // 搜索笔记
    onSearch() {
      this.$emit('search')
    },
    // 新建笔记
    createFile() {
      this.$emit('create')
    },
    // 导入文件
    importFile() {
      this.$emit('import')
    }
  }
}
</script>

<style lang="less" scoped>
.search-container {
  display: flex;
  align-items: center;
  padding: 12px 10px;
  background: #daecfe;

  .el-dropdown {
    .el-button--small {
      margin-left: 10px;
      padding: 6px;
      font-size: 14px;
      border-radius: 30%;
    }
  }
}
</style>
