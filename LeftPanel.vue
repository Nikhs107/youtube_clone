<template>
  <div class="hello">
   <header><i class="fab fa-youtube"></i>MyYouTube</header>
    <ul>
      <li @click="handleChange('1')">List</li>
      <li @click="handleChange('2')">Upload</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'LeftPanel',
  props: {
    handleChange: Function,
  },
}
</script>

<style scoped>
header {
  color: darkred;
  font-size: 2rem;
}
ul {
  list-style-type: none;
  padding: 0;
  margin-top: 50px;
}
li {
  margin: 10px;
  font-size: 1.5rem;
  border-radius: 50px;
  background: gray;
  color: aliceblue;
  cursor: pointer;
}
li:hover {
  color: aquamarine;
  background: dimgray;
}
</style>
