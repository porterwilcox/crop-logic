<template>
  <nav class="navigation navbar navbar-expand-lg">
    <!-- logo(s) -->
    <div class="ml-3">
      <a class="navbar-brand" href="#">
        <img
          src="https://croplogic.com/cl/wp-content/uploads/2019/04/CropLogic-Logo_APPLE-GREEN.png"
          alt="crop-logc-logo"
        />
      </a>
      <a class="navbar-brand" href="#" v-if="$mq > 1">
        <img
          src="https://croplogic.com/cl/wp-content/uploads/2019/04/ProAgCropLogic-Logo_FORREST-GREEN.png"
          alt="crop-logc-logo"
        />
      </a>
      <a class="navbar-brand" href="#" v-if="$mq != 4 && $mq > 1 ">
        <img
          src="https://croplogic.com/cl/wp-content/uploads/2019/04/Logical-Cropping_Yellow.png"
          alt="crop-logc-logo"
        />
      </a>
    </div>
    <!-- /logo(s) -->
    <div class="d-flex justify-content-center">
      <div class="dropleft navbar-toggler">
        <i class="fas fa-search text-green nav-link" data-toggle="dropdown"></i>
        <div class="dropdown-menu mt-5" style="width: 250px;">
          <div class="input-group d-flex justify-content-center">
            <input autofocus type="text" placeholder="Search" class="text-green" />
            <div class="input-group-append">
              <i class="input-group-text bg-green fas fa-search text-white"></i>
            </div>
          </div>
        </div>
      </div>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <i class="fas fa-bars"></i>
      </button>
    </div>

    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav ml-auto row align-items-center">
        <li class="nav-item">
          <a class="nav-link text-green h6" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-green h6" href="#">About Us</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-green h6" href="#">Our Products</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-green h6" href="#">Investor Relations</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-green h6" href="#">News</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-green h6" href="#">Contact</a>
        </li>
        <li class="nav-item">
          <a class="nav-link h6 btn bg-green text-white" href="#">Client Login</a>
        </li>
        <li v-if="$mq > 3" class="dropleft nav-item mr-5 action">
          <i class="fas fa-search text-green nav-link" data-toggle="dropdown"></i>
          <div class="dropdown-menu mt-5" style="width: 250px;">
            <div class="input-group d-flex justify-content-center">
              <input autofocus type="text" placeholder="Search" class="text-green" />
              <div class="input-group-append">
                <i class="input-group-text bg-green fas fa-search text-white"></i>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "navigation",
  props: [],
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: {}
};
</script>

<style>
input[placeholder="Search"], input[placeholder="Search"]:active, input[placeholder="Search"]:focus {
    background: var(--baige);
    border: 1px solid lightgrey;
    outline: none;
    height: 30px;
}
input[placeholder="Search"]::placeholder {
    color: var(--green);
}
</style>