<template>
<body>
  <div class="container-fluid">
    <div class="row my-5">
      <div class="col-lg-6 box">
        <nuxt-link to="/alat">
          <div class="card bg-alat rounded-5">
            <div class="card-body">
              <h2 class="btn btn-secondary fs-3 rounded-3">PINJAM ALAT</h2>
            </div>
          </div>
        </nuxt-link>
      </div>
      <div class="col-lg-6 box ">
        <nuxt-link to="../ruang">
          <div class="card bg-ruang rounded-5">
            <div class="card-body">
              <h2 class="btn btn-secondary fs-3 rounded-3">PINJAM RUANG</h2> 
            </div>
          </div>
        </nuxt-link>
      </div>
    </div>
    <div class="row my-6">
      <div class="col-lg-6 box">
        <nuxt-link to="../sop">
          <div class="card bg-sop rounded-5">
            <div class="card-body">
              <h2 class="btn btn-secondary fs-3 rounded-3">SOP</h2>
            </div>
          </div>
        </nuxt-link>
      </div>
      <div class="col-lg-6 box ">
      <nuxt-link to="../riwayat">
        <div class="card bg-riwayat rounded-5">
          <div class="card-body">
            <h2 class="btn btn-secondary fs-3 rounded-3">RIWAYAT</h2> 
          </div>
        </div>
      </nuxt-link>
    </div>
  </div>
    
  </div>
</body>
</template>

<style scoped>
body {
  background-color: #b4b4b4;
  padding: 5px;
  width: 100%;
  height: 100%;
}
.card{
  height: 450px;
  box-shadow: 2px 2px 20px white;
}
.card.bg {
  padding: 5px;
  margin: 5px;
}
.card.bg-alat {
  background-image: url('../assets/img/alat.png');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}
.card.bg-ruang {
  background: url('../assets/img/ruang.png') no-repeat center center;
  background-size: cover;
}
.card.bg-sop {
  background-image: url('../assets/img/sop.png');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}
.card.bg-riwayat {
  background-image: url('../assets/img/ruang.png');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}
</style>
