<template>
  <div class="box df jc_c ai_c">
    <div class="df box1">
      <el-col :span="8">
        <el-card>
            <div class=" flx df jc_b mr">
                <span class=" iconfont icon-duoren" style="color:green"></span>
                <div>
                    <div class="mb">messagess</div>
                    <div class="mt count">
                        <countTo :startVal="startVal" :endVal='count.message' :duration='3000'></countTo>
                    </div>
                </div>
            </div>
        </el-card>
      </el-col>
    </div>
  </div>
</template>

<script>
import countTo from "vue-count-to";

export default {
  name: "",
  props: {
    count: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      startVal: 0,
    };
  },
  components: {
    countTo,
  },
  methods: {},
  mounted() {},
  computed: {},
  watch: {},
};
</script>

<style lang='scss' scoped>
.box{
    padding: 30px 15px;
    .box1{
        width: 100%;
    }
}
</style>