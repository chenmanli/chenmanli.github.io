<template>
  <div class="translateform">
    <form v-on:submit="formsubmit">
    <input type="text" v-model="texttotranslate" placeholder="请输入需要翻译是内容">
     <select>
     <option value="en">en</option>
      
     </select>
      <input type="submit" value="翻译">
      </form>
     </div>
    </template>
<script>
export default {
  name: 'translateform',
  data () {
    return {
     texttotranslate:""

    }
  },
  methods:{
  formsubmit:function(e){
  //alert(this.texttotranslate);
  e.preventDefault();
  this.$emit("formsubmit",this.texttotranslate);
  }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


</style>
