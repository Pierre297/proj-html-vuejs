<template>
  <div>
    <div class="works-container">
      <div class="card">
        <img :src="require('../assets/' + work.image)" :alt="work.title" />
      </div>
      <div class="overlay text">
        <div class="icon">
          <div class="circle"><i class="fas fa-link"></i></div>
          <div class="circle"><i class="fas fa-search"></i></div>
        </div>
        <h4>Florida Health Facility</h4>
        <p>Commercial</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "RecentWork",
  props: {
    work: Object,
  },
};
</script>

<style scoped lang="scss">
.works-container {
  font-size: 20px;
  margin-top: 100px;
  width: 300px;
  position: relative;

  img {
    width: 100%;
  }
}

// display testo hover
.overlay {
  position: absolute;

  bottom: 0;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: 0.5s ease;
  background-color: #fed03d;
}

.works-container:hover .overlay {
  opacity: 1;
  cursor: pointer;
}

.text {
  position: absolute;
  color: #1e1e1e;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  text-align: center;

  p {
    color: #1e1e1e;
    width: 80%;
    margin-left: 10%;
    margin-bottom: 20px;
    color: white;
  }
  h4 {
    padding-top: 45px;
    width: 80%;
    margin-left: 10%;
    color: white;
  }
}

.circle {
  background-color: white;
  border-radius: 50%;
  width: 50px;
  height: 50px;
  display: inline-block;
  margin: 0 10px;
  margin-top: 30px;

  i {
    padding-top: 15px;
  }
}
</style>