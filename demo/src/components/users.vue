<template>
  <div class="users">
  <h1>this is users</h1>
    <ul>
    <li v-for="user in users">
    <h2>{{user.name}}</h2>
    <h3 >{{user.email}}</h3>
    </li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'users',
  //props:["users"]属性传递
  props:{
  users:{
  type:Array,
  require:true
  }
  },
  data () {
    return {
      
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.users{
	width:100%;
	max-width:1200px;
	margin:40px auto;
	padding:0 20px;
	box-sizing:border-box;
}
ul{
	
	display:flex;
	list-style-type:none;
	flex-wrap:wrap;
	padding:0;
}
li{
	margin:10px;
	padding:30px;
	border:1px solid #222;
	text-align:center;
	flex-grow:1;
	flex-basis:200px;
}

</style>
