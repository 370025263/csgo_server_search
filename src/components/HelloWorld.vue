<template>
  <div>
    <p v-on:click="give_father">[HIT ME TO GIVE FATHER DATA]</p>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return{
      va:"SON DATA"
    }
  },
  methods:{
    give_father:function () {
      alert("ddd")
      var out_d = this.va
      this.$emit("data_sent", out_d)
    }

  }

}
</script>

