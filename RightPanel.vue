<template>
  <div class="hello">
    <div v-if="view==='1'">
        <PlayList/>
    </div>
    <div v-if="view==='2'">
        <Upload/>
    </div>
  </div>
</template>

<script>
import PlayList from "./PlatList.vue";
import Upload from "./Upload.vue"
export default {
  name: "RightPanel",
  components:{
      PlayList,
      Upload
  },
  props:{
      view:String
  }
};
</script>

<style scoped>

</style>
