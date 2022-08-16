<template>
  <el-table :data="tableData" border style="width: 100%">
    <el-table-column
      fixed
      :prop="item.prop"
      :label="item.label"
      :width="item.width"
      v-for="(item, index) in titleData"
      :key="index"
    >
    </el-table-column>
    <!--<el-table-column prop="name" label="姓名" width="120"> </el-table-column>
        <el-table-column prop="province" label="省份" width="120"></el-table-column>
        <el-table-column prop="city" label="市区" width="120"> </el-table-column>
        <el-table-column prop="address" label="地址" width="300"> </el-table-column>
        <el-table-column prop="zip" label="邮编" width="120"> </el-table-column> -->

    <el-table-column fixed="right" label="操作">
      <template slot-scope="scope">
        <el-button @click="handleClick(scope.row)" type="text" size="small"
          >查看</el-button
        >
        <el-button type="text" size="small">编辑</el-button>
      </template>
    </el-table-column>
  </el-table>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    tableData: {
      type: Array,
      required: true,
    },
    titleData: {
      type: Array,
      required: true,
    },
  },
  methods: {
    handleClick(row) {
      console.log(row);
    },
  },
};
</script>
