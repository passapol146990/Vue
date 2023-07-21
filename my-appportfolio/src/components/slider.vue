<template>
  <div class="box">
    <div class="boxin">
        <div class="col-lg-3"></div>
      <div class="carousel slide col-lg-6" id="carousel" data-bs-ride="carousel">
        <ol class="carousel-indicators">
            <button data-bs-target="#carousel" data-bs-slide-to="1" class="active"></button>
            <button data-bs-target="#carousel" data-bs-slide-to="2"></button>
            <button data-bs-target="#carousel" data-bs-slide-to="3"></button>
        </ol>
        <div class="carousel-inner container">
            <div class="carousel-item active">
                <img src="./assets/1.jpg">
            </div>
            <div class="carousel-item">
                <img src="./assets/2.jpg">
            </div>
            <div class="carousel-item">
                <img src="./assets/3.jpg">
            </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "sliderVue",
};
</script>

<style scoped>
.box {
  left: 0;
  width: 100%;
  height: 720px;
}
.boxin {
  margin-top: 54px;
  display: flex;
}
.carousel-inner img{
    width: 100%;
}
</style>