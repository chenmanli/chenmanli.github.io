<template>
  <div id="app">
  <ul>
   <li><router-link to="/">home</router-link></li>
   <li><router-link to="/helloworld">hello</router-link></li>
  </ul>
   <router-view></router-view>
  </div>
</template>

<script>
//注册局部组件


export default {
  name: 'App',
  data(){
    return{

      title:"这是我的第一个ceshe"
    }
  }
}
</script>

<style scoped>
h1{
  color:green;
}

</style>
