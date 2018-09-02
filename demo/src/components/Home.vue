<template>
  <div id="home">
   <app-header v-on:titlechang="updatetitle($event)"
   v-bind:title="title"></app-header>
   <users v-bind:users="users"></users>
   <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
//注册局部组件
import users from './users'
import header from './header'
import footer from './footer'
export default {
  name: 'Home',
  data(){
    return{
    users:[
      //{name:"hen",job:"web 开发",show:false},
      //{name:"hen",job:"web 开发",show:false},
      //{name:"hen",job:"web 开发",show:false},
      //{name:"hen",job:"web 开发",show:false},
      //{name:"hen",job:"web 开发",show:false}
      ],
      title:"这是我的第一个ceshe"
    }
  },
  methods:{
  updatetitle:function(title){
    this.title=title;
  }
  },
  components:{
  "users":users,
  "app-header":header,
  "app-footer":footer
  },
  created(){
  this.$http.get("http://jsonplaceholder.typicode.com/users")
  .then((data)=>{
  this.users=data.body;
  })
  }
}
</script>

<style scoped>
h1{
  color:green;
}

</style>
