<template>
  <div class="home container-fluid">
    <div id="home-carousel" data-interval="4800" class="carousel slide row" data-ride="carousel">
      <ol class="carousel-indicators">
        <li data-target="#home-carousel" data-slide-to="0" class="active"></li>
        <li data-target="#home-carousel" data-slide-to="1"></li>
        <li data-target="#home-carousel" data-slide-to="2"></li>
      </ol>
      <div class="carousel-inner position-relative">
        <div class="caro-text-container h-100 position-absolute w-100 d-flex justify-content-center align-items-center">
          <h2 class="caro-text">SCIENCE. AGRONOMY. TECHNOLOGY.</h2>
        </div>
        <div class="carousel-item active">
          <img src="https://croplogic.com/cl/wp-content/uploads/2018/10/CL_Website-Banner_1500x430_realTime-app_01.jpg"
            class="d-block w-100" alt="" />
        </div>
        <div class="carousel-item">
          <img
            src="https://croplogic.com/cl/wp-content/uploads/2018/10/CL_Website-Banner_1500x430_Roger-McCary-and-Chris-Friberg.jpg"
            class="d-block w-100" alt="" />
        </div>
        <div class="carousel-item">
          <img
            src="https://croplogic.com/cl/wp-content/uploads/2018/10/CL_Website-Banner_1500x430_sensor-probe_apple-01.jpg"
            class="d-block w-100" alt="" />
        </div>
      </div>
      <a class="carousel-control-prev" href="#home-carousel" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#home-carousel" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
    <div class="row justify-content-center bg-baige">
      <div class="col-11">
        <div class="row justify-content-between" :class="{'flex-column': $mq < 3}">
          <div class="col-12 col-lg-4">
            <div class="card">
              <div class="card-header-container">
                <img src="https://croplogic.com/cl/wp-content/uploads/2019/03/CL_Product-Feature_495x400_staff_01.jpg"
                  class="card-img-top">
                <h4 class="centered">Our Story</h4>
              </div>
              <div class="card-body text-center">
                <p class="text-black">CropLogic is an award-winning global digital ag-tech company specialising in soil
                  moisture management solutions. <a href="#" class="text-link-green">View our story.</a></p>
              </div>
            </div>
          </div>
          <div class="col-12 col-lg-4">
            <div class="card card2">
              <div class="card-header-container">
                <img
                  src="https://croplogic.com/cl/wp-content/uploads/2019/04/CL_Product-Feature_495x400_realTime_03.jpg"
                  class="card-img-top">
                <h4 class="centered">Crop Logic Realtime</h4>
              </div>
              <div class="card-body text-center">
                <p class="text-black">Powerfully simple, actionable in-field information designed to help growers
                  optimise crop profitability.<a href="#" class="text-link-green">Find out more.</a></p>
              </div>
            </div>
          </div>
          <div class="col-12 col-lg-4">
            <div class="card card3">
              <div class="card-header-container">
                <img
                  src="https://croplogic.com/cl/wp-content/uploads/2019/01/CL_Product-Feature_495x400_Sam-Kniveton.jpg"
                  class="card-img-top">
                <h4 class="centered">Our Team</h4>
              </div>
              <div class="card-body text-center">
                <p class="text-black">At CropLogic we are a global team with over 100 years combined experience across
                  Australia and USA. <a href="#" class="text-link-green">View our team member stories here.</a></p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "home",
    components: {}
  };
</script>

<style scoped>
  .caro-text-container {
    z-index: 1;
    animation: caption-left 1s 1 cubic-bezier(0.985, 0.005, 0.265, 1);
    left: -100%;
    animation-fill-mode: forwards;
  }

  @keyframes caption-left {
    100% {
      left: 0;
    }
  }

  .caro-text {
    font-size: 3vw;
    color: white;
    border: 3px solid white;
    font-family: 'oswald', 'HelveticaNeue', 'Helvetica Neue', 'Helvetica-Neue', Helvetica, Arial, sans-serif;
  }

  .card-img-top {
    transition: all .5s;
    border-radius: 3%;
    filter: brightness(75%);
  }

  .card-header-container:hover .card-img-top {
    filter: brightness(100%);
  }

  .card {
    opacity: 0;
    position: relative;
    top: -50px;
    border: 10px solid white;
    border-radius: 5%;
    min-height: fit-content;
    height: 100%;
    box-shadow: 0 0 1px lightgrey;
    animation: fade-appear .75s cubic-bezier(0.985, 0.005, 0.265, 1) 1 normal forwards;
    z-index: 16;
  }

  @media(max-width: 768px) {
    .card {
      top: 0;
      margin: 1rem 0;
    }
  }

  .card2 {
    animation-delay: .05s;
  }

  .card3 {
    animation-delay: .1s;
  }


  @keyframes fade-appear {
    100% {
      opacity: 1;
    }
  }

  .card-header-container {
    position: relative;
    text-align: center;
    color: white;
    cursor: pointer;
  }

  .centered {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-family: 'oswald', 'HelveticaNeue', 'Helvetica Neue', 'Helvetica-Neue', Helvetica, Arial, sans-serif;
    text-transform: uppercase;
  }
</style>