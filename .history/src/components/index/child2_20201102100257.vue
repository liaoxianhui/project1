<template>
  <div>
    <el-row :gutter="20">
      <el-col style="width:100%">
        <el-card>
          <ve-line :data="chartData" :settings="chartSettings"></ve-line>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: "",
  props: {
    line: {
      type: Array,
    },
  },
  data() {
    this.chartSettings = {
      metrics: ["expected", "actual"],
      dimension: ["data"],
    };
    return {
      chartData: {
        columns: ["data", "expected", "actual"],
        rows: [],
      },
    };
  },
  components: {},
  methods: {},
  mounted() {
    this.chartData.rows = this.line;
  },
  computed: {},
  watch: {},
};
</script>

<style lang='scss' scoped>
</style>