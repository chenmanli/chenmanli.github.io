<template>
  <div class="translateoutput">
    
    {{translatedtext}}

  </div>
</template>

<script>
export default {
  name: 'translateoutput',
  data () {
    return {

    }
  },
  props:[
  "translatedtext"
  ]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


</style>
