<template>
  <header>
    <h1 v-on:click="changtitle">vue.js {{title}}</h1>
  </header>

</template>

<script>
export default {
  name: 'header',
  props:{
  title:{
  type:String
  }
  },
    data () {
    return {
      
      
    }
  },
  methods:{
  changtitle:function(){
  //this.title="changedetitle";
  this.$emit("titlechang","子向父传值");
  }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header{
	background:lightgreen;
	padding:10px;
}
h1{
	color:#222;
	text-align:center;
}

</style>