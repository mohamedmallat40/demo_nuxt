<template>
  <div class="container-login absolute -top-0 h-16 bg-white shadow-lg">
    <div class="line -top-0 w-screen"></div>
    <p class="float-right mt-4 mr-3 cursor-pointer login hover:underline">
      Login
    </p>
  </div>
</template>

<script>
export default {}
</script>

<style>
.container-login {
  border-radius: 0px 0px 12px 12px;
}
.line {
  background: transparent linear-gradient(91deg, #319795 0%, #3182ce 100%) 0% 0%
    no-repeat padding-box;
  height: 5px;
}
.login {
  letter-spacing: 0.84px;
  color: #319795;
  font-weight: 600;
}
</style>
