<template>
  <div id="app">
    <MyForm :tableData="tableData" :titleData="titleData"/>
  </div>
</template>

<script>
import MyForm from "./components/MyForm.vue";

export default {
  name: "App",
  components: {
    MyForm,
  },
  data() {
    return {
      titleData: [
        {
          prop: "id",
          label: "序号",
          width: "150",
        },
        {
          prop: "date",
          label: "日期",
          width: "150",
        },
        {
          prop: "name",
          label: "姓名",
          width: "150",
        },
        {
          prop: "province",
          label: "省份",
          width: "150",
        },
        {
          prop: "city",
          label: "市区",
          width: "150",
        },
        {
          prop: "address",
          label: "地址",
          width: "150",
        },
        {
          prop: "zip",
          label: "邮编",
          width: "150",
        },
      ],
      tableData: [
        {
          id:'1',
          date: "2016-05-02",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },{
          id:'2',
          date: "2016-05-02",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          id:'3',
          date: "2016-05-02",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          id:'4',
          date: "2016-05-02",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          id:'5',
          date: "2016-05-02",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          id:'6',
          date: "2016-05-02",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          id:'7',
          date: "2016-05-02",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          id:'8',
          date: "2016-05-02",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        },
        {
          id:'9',
          date: "2016-05-02",
          name: "王小虎",
          province: "上海",
          city: "普陀区",
          address: "上海市普陀区金沙江路 1518 弄",
          zip: 200333,
        }
      ],
     
    };
  },
};
</script>

<style></style>
