<template>
  <div class="home h-screen w-screen">
    <div class="flex h-full">
      <div class="contenu mt-16">
        <div class="text m-auto">
          <h1 class="title text-center font-bold">Deine Job website</h1>
        </div>
        <div class="w-screen flex justify-center">
          <div class="image"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'homeVue',
}
</script>

<style scoped>
.home {
  background: transparent linear-gradient(141deg, #ebf4ff 0%, #e6fffa 100%) 0%
    0% no-repeat padding-box;
}
.image {
  background: transparent url('/img/undraw_agreement_aajr.svg') 0% 0% no-repeat
    padding-box;
  width: 418px;
  height: 405px;
  max-width: 100vw;
}
.text {
  width: 320px;
}
.title {
  letter-spacing: 1.26px;
  color: #2d3748;
  font-size: 50px;
}
</style>
