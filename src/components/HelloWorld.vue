<template>
  <div class="hello">
     <input type="" :placeholder="this.msg"/>
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg:""
    }
  },
  mounted() {
  	    let than = this;
        than.axios.get("/api/newData").then((res) =>{
        		than.msg=res.data.dataInfo.state;
            console.log(than.msg)
        })
        
   },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
