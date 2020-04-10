<template>
  <div>
    <el-row :gutter="20">
      <el-col :span="4">
        <el-input v-model="input" placeholder="请输入客户名字" />
      </el-col>
      <el-col :span="4">
        <el-button type="primary">查询</el-button>
      </el-col>
      <el-col :span="4">
        <el-button type="primary">新增</el-button>
      </el-col>
      <el-col :span="4">
        <el-button type="primary">导出</el-button>
      </el-col>
    </el-row>
    <el-table :data="tableData" border style="width: 100%;top:20px">
      <el-table-column prop="name" label="客户名称" width="200" />
      <el-table-column prop="up" label="上级" width="220" />
      <el-table-column prop="province" label="机构代码" width="220" />
      <el-table-column prop="city" label="公司法人" width="220" />
      <el-table-column prop="address" label="地址" width="300" />
      <el-table-column prop="zip" label="邮编" width="220" />
      <el-table-column fixed="right" label="操作" width="200">
        <template slot-scope="scope">
          <el-button type="text" size="small" @click="handleClick(scope.row)">查看</el-button>
          <el-button type="text" size="small">编辑</el-button>
          <el-button type="text" size="small">访客记录</el-button>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>
<script>
export default {

  data() {
    return {
      input: '',
      tableData: [
        {
          name: '王小虎',
          up: 'ddd',
          province: '3123dasdada',
          city: '王晓丽',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        },
        {
          name: '王小虎',
          up: 'ddd',
          province: '3123dasdada',
          city: '王晓丽',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        },
        {
          name: '王小虎',
          up: 'ddd',
          province: '3123dasdada',
          city: '王晓丽',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        },
        {
          name: '王小虎',
          up: 'ddd',
          province: '3123dasdada',
          city: '王晓丽',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        }
      ]
    }
  },
  methods: {
    handleClick(row) {
      console.log(row)
    }
  }
}
</script>
<style lang="scss" scoped>

</style>
