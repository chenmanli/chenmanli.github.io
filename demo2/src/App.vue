<template>
  <div id="app">
  <h1>在线翻译</h1>
  <h5>简单/易用/便捷</h5>
   <translateform v-on:formsubmit="translatetext"></translateform>
    <translateoutput v-text="translatedtext"></translateoutput>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import translateform from './components/translateform'
import translateoutput from './components/translateoutput'

export default {
  name: 'App',
  data:function(){
  return{
   translatedtext:""
  }
  },
  components: {
   translateform,
   translateoutput
  },
  methods:{
  translatetext:function(text){
  //alert(text);
  this.$http.get('https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20180611T041751Z.761a657e2b451443.1c8c07e511b6d3bf8a5744cf21be71903bb64489&lang=en&text='+text)
  .then((response)=>{
     this.translatedtext=response.body.text[0];
  })
  }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
