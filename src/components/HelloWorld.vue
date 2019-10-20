<template>
  <div>
    <el-row :gutter="20" type="flex" justify="center" align="middle">
      <el-col :span="6">
        <el-input placeholder="Please input" v-model="post.url">
          <template slot="prepend">Http://</template>
        </el-input>
      </el-col>
      <el-col :span="5"> 
        <el-input placeholder="Please input" v-model="post.name"></el-input>
      </el-col>
      <el-col :span="3"><el-button type="primary" round @click="addPost">Ekle</el-button></el-col>

      
    </el-row>
  </div>
</template>

<script>

  import {eventBus} from "../main";
  export default {
   component:{

   },
   data(){
    return{
      post:{
        name:null,
        url:null
      }
    }
  },
  methods:{
    addPost() {

      eventBus.$emit("postAdd", this.post);
      
    }
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
