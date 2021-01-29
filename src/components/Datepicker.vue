<template>
  <div class="block">
    <p>dasdasdasdasdasdasdjhgsdfhanvhsdibhdigiughbiubishglhboibgigibay</p>
    <span class="demonstration">起始日期时刻为 12:00:00</span>
    <el-date-picker
        v-model="value1"
        type="datetimerange"
        start-placeholder="开始日期"
        end-placeholder="结束日期"
        :default-time="['12:00:00']">
    </el-date-picker>
  </div>

</template>

<script>
import
export default {
  data() {
    return {
      value1: '',
      value2: ''
    };
  },
  methods:{
    send_data:function(){
      var data_time = [this.value1,this.value2]
      this.$emit('event_send',data_time)
    }

  },
  watch:{
    'value1':function () {
      this.send_data()

    },
    'value2':function () {
      this.send_data()
    }

  }

};
</script>