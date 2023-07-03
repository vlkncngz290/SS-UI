<template>
  <div class="container-fluid">
    <div class="row flex-nowrap">
      <div class="bg-light col-auto col-md-3 col-lg-3 min-vh-100">
        <div class="bg-light mt-3">
          <a class="d-flex justify-content-center" href="/">
            <img
              src="/SSLogo.png"
              height="45"
              alt="MDB Logo"
              loading="lazy"
            />
          </a>
          <hr class="hr hr-blurry"/>
          <ul class="nav nav-pills flex-column">
            <li class="card">
              <a href="/dashboard" class="link-secondary mx-3 mt-1 mb-1"><i class="fas fa-1x fa-house-chimney-user "></i><span class="h6 ms-3">Dashboard</span></a>
            </li>
            <li class="card mt-3">
              <a href="/buy" class="link-secondary mx-3 mt-1 mb-1"><i class="fas fa-1x fa-credit-card "></i><span class="h6 ms-3">Buy</span></a>
            </li>
            <li class="card mt-3">
              <a href="/predictions" class="link-secondary mx-3 mt-1 mb-1"><i class="fas fa-1x fa-arrow-trend-up "></i><span class="h6 ms-3">Predictions</span></a>
            </li>
            <li class="card mt-3">
              <a href="/temp" class="link-secondary mx-3 mt-1 mb-1"><i class="fas fa-1x fa-house-chimney-user"></i><span class="h6 ms-3">Temp</span></a>
            </li>
          </ul>
        </div>
      </div>
      <div class="p-3">
        <Nuxt/>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: "user"
}
</script>

<style scoped>

</style>
