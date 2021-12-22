<template>
<div class="hello">
<header>Video Uploader</header>
<hr>
  <div class="container">
    <h2>Select a Video</h2>
    <input type="file" @change="handleChange" /><br />
    <button @click="upload">Upload File</button>
  </div>
</div>
</template>

<script>
import axios from "axios";

export default {
  name: "Upload",
  data() {
    return {
      video: "",
      uploadURL: "",
    };
  },
  created() {
    axios
      .get(
        "https://q5907y2vzc.execute-api.ap-south-1.amazonaws.com/default/testing_function_107"
      )
      .then((res) => {
        this.uploadURL = res.data.uploadURL;
      });
  },
  methods: {
    handleChange(e) {
      let files = e.target.files || e.dataTransfer.files;
      this.video =files[0];
    },
    
    upload() {
      axios.put(this.uploadURL, this.video).then((res) => {
        alert("File is uploaded to S3 bucket");
        console.log(res);
      });
    },
  },
};
</script>

<style scoped>
h2 {
  color: darkred;
}
.container {
  width: 50%;
  margin: 100px auto;
  padding: 10px;
  border: 1px solid black;
  border-radius: 10px;
  background-color: lightsalmon;
  font-size: 1.5em;
}
input,
button {
  width: 100%;
  padding: 10px;
  margin: 10px auto;
  border: 1px solid gray;
  box-sizing: border-box;
  font-size: 1em;
  border-radius: 5px;
}
input {
  background-color: lightcyan;
}
button{
  cursor: pointer;
}
header {
  color: white;
  font-size: 2rem;
  background: black;
  height: 70px;
  margin: 0 10px;
  border-radius: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>