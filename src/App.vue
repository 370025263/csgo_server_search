<template>
  <div id="app">
    <p>FATHER: {{f_time}}   {{t_time}}</p>
    <Datepicker @event_send="get_data" v-show="true" ></Datepicker>
  </div>
</template>

<script>
import Datepicker from './components/Datepicker.vue'

export default {
  name: 'App',
  data(){
    return {
      f_time:'',
      t_time:''
    }
  },
  components: {
    Datepicker
  },
  methods:{
    get_data:function (value) {
      alert("got")
      this.f_time = value.value1
      this.t_time = value.value2
    }
  }
}
</script>

