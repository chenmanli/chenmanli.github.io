<template>
    <footer>
     <p>{{copyright}}{{title}}</p>

    </footer>
</template>

<script>
export default {
  name: 'footer',
  props:{
  title:{
  type:String
  }
  },
  data () {
    return {
      copyright:"copyright 2017 vue demo"
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
footer{
	background:black;
	padding:6px;
}
p{
	color:lightgreen;
	text-align:center;

}
</style>
