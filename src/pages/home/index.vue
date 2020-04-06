<template>
  <div id="app">
    <div>scroll down↓</div>
    <div style="height: 1500px;"></div>
    <el-table border stripe :data="data">
      <el-table-column
        v-for="i in 10"
        :key="i"
        :label="'label' + i"
        :prop="String(i)"
        sortable
        resizable
        align="center"
        :filters="[{text: 'a', value: 'a'}]"
      ></el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data: function() {
    return {
      data: Array(5).fill({
        1: "a",
        2: "b",
        3: "c",
        4: "d",
        5: "e",
        6: "f",
        7: "g",
        8: "h",
        9: "i",
        10: "j"
      })
    };
  }
};
</script>
