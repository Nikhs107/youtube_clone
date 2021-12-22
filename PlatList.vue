<template>
  <div class="hello">
    <header>My List</header>
    <hr />
    <div class="list-items">
      <div class="card">
        <div class="card-video">
          <video controls>
            <source src="../assets/myVideo.mp4" type="video/mp4" />
          </video>
        </div>
        <div class="card-title">Video1</div>
      </div>
      <div class="card">
        <div class="card-video">
          <video controls>
            <source src="../assets/myVideo.mp4" type="video/mp4" />
          </video>
        </div>
        <div class="card-title">Video2</div>
      </div>
      <div class="card">
        <div class="card-video">
          <video controls>
            <source src="../assets/myVideo.mp4" type="video/mp4" />
          </video>
        </div>
        <div class="card-title">Video3</div>
      </div>
      <div class="card">
        <div class="card-video">
          <video controls>
            <source src="../assets/myVideo.mp4" type="video/mp4" />
          </video>
        </div>
        <div class="card-title">Video4</div>
      </div>
      <div class="card">
        <div class="card-video">
          <video controls>
            <source src="../assets/myVideo.mp4" type="video/mp4" />
          </video>
        </div>
        <div class="card-title">Video5</div>
      </div>
      <div class="card">
        <div class="card-video">
          <video controls>
            <source src="../assets/myVideo.mp4" type="video/mp4" />
          </video>
        </div>
        <div class="card-title">Video6</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PlayList",
};
</script>

<style scoped>
.list-items {
  margin: 10px 50px;
  width: 100%;
}
.card:hover {
  color: aquamarine;
  background: dimgray;
}
.card {
  width: 30%;
  height: 30vh;
  float: left;
  margin: 10px;
  font-size: 1.5rem;
  border-radius: 5px;
  background: gray;
  color: aliceblue;
  cursor: pointer;
}
video{
    width: 100%;
    height: 26vh;
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
