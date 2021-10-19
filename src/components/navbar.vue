<template>
  <div id="navbar">
    <nav id="nav" class="navbar navbar-expand-lg navbar-light nav">
      <div class="container-fluid">
        <router-link class="navbar-brand" to="/"
          ><img  alt="logo"
        /></router-link>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <i class="fa fa-bars" aria-hidden="true"></i>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mb-2 mb-lg-0 mlauto">
            <li class="nav-item">
              <router-link class="nav-link active" to="/"
                ><b>Home</b></router-link
              >
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/"><b>Login</b></router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>
<script>
export default {
  name: "navbar",
  
};
</script>

<style>
.navbar {
  display: flex;
  height: 60px;
  background-image: linear-gradient(to right, #3931af, #00c6ff);
  padding: 0px !important;
  width: 100%;
}
#nav .nav-item {
  margin-right: 40px;
}
.mlauto {
  margin-left: auto;
}
.navbar-brand img {
  height: 90px;
  padding: 5px;
}
.navbar-nav li .nav-link {
  color: white !important;
}
.navbar-nav li router-link {
  color: white !important;
  font-weight: 600;
}
.fa-bars {
  color: #fff;
}
#nav .btn-outline-success {
  background-color: #19029b;
  border-radius: 10px;
  border: none;
  padding: 8px 25px;
  box-shadow: none;
  width: auto;
  margin: auto;
  color: white;
}

/* Add Zoom Animation */
.astext {
  background: none;
  border: none;
  margin: 0;
  cursor: pointer;
}
.nav-link {
  padding-top: 15px;
  color: white;
}
img {
  height: 30px;
  border: none;
}
span {
  border: none;
}
span:hover {
  cursor: pointer;
}
#nav .input-group {
  margin: auto;
}
.searchdiv {
  margin: auto;
}
.logoutdiv:hover {
  cursor: pointer;
}
</style>
