<template>
  <div class="container-register bg-white w-screen flex justify-center">
    <button class="m-auto register">Kostenlos Registrieren</button>
  </div>
</template>

<script>
export default {}
</script>

<style>
.container-register {
  border-radius: 12px 12px 0px 0px;
  box-shadow: 0px -1px 3px #00000033;
  padding: 1.5rem;
  position: fixed;
  bottom: 0;
  z-index: 999;
}

.register {
  letter-spacing: 0.84px;
  color: #e6fffa;
  background: transparent linear-gradient(95deg, #319795 0%, #3182ce 100%) 0% 0%
    no-repeat padding-box;
  padding: 0.8rem 4rem;
  border-radius: 12px;
}
.register:hover {
  opacity: 0.7;
}
</style>
