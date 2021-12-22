<template>
  <div id="app">
    <div class="container">
      <div class="left">
        <LeftPanel :handleChange="setView"/>
      </div>
      <div class="right">
        <RightPanel :view="choice"/>
      </div>
    </div>
  </div>
</template>

<script>
import LeftPanel from "./components/LeftPanel.vue";
import RightPanel from "./components/RightPanel.vue";

export default {
  name: "App",
  components: {
    LeftPanel,
    RightPanel,
  },
  data(){
    return{
      choice:'1'
    }
  },
  methods:{
    setView(ch){
      this.choice = ch;
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.left {
  width: 20%;
  height: 900px;
  float: left;
  background: rgb(247, 228, 231);
}
.right {
  width: 80%;
  height: 900px;
  float: left;
  background: lightyellow;
}
</style>
