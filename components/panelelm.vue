<template>
  <div>
    <div class="title m-auto mt-3">
      <h2 class="text-center font-medium">{{ h2 }}</h2>
    </div>
    <div class="item">
      <div class="flex justify-center">
        <img class="mb-6rem" :src="`img/${img1}.svg`" alt="" />
      </div>

      <p class="flex mb-5">
        <span class="number mr-4">1.</span>
        <span class="mt-auto"> {{ p1 }}</span>
      </p>
    </div>
    <svg
      class="-mb-5rem"
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 1440 320"
    >
      <path
        fill="#ffffff"
        fill-opacity="1"
        d="M0,160L48,181.3C96,203,192,245,288,250.7C384,256,480,224,576,176C672,128,768,64,864,37.3C960,11,1056,21,1152,58.7C1248,96,1344,160,1392,192L1440,224L1440,0L1392,0C1344,0,1248,0,1152,0C1056,0,960,0,864,0C768,0,672,0,576,0C480,0,384,0,288,0C192,0,96,0,48,0L0,0Z"
      ></path>
    </svg>
    <div class="item2">
      <p class="flex mb-5">
        <span class="number text-center ml-3rem w-widescreen mr-4">2.</span>
        <span class="mt-auto"> {{ p2 }}</span>
      </p>

      <div class="flex justify-center">
        <img class="mt-3" :src="`img/${img2}.svg`" alt="" />
      </div>
      <svg
        class="-mt-2rem"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1440 320"
      >
        <path
          fill="#fff"
          fill-opacity="1"
          d="M0,224L48,213.3C96,203,192,181,288,192C384,203,480,245,576,266.7C672,288,768,288,864,266.7C960,245,1056,203,1152,181.3C1248,160,1344,160,1392,160L1440,160L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
        ></path>
      </svg>
    </div>

    <p class="ml-8 flex mb-4">
      <span class="number ml-6 mr-4">3.</span>
      <span class="mt-auto">{{ p3 }}</span>
    </p>

    <div class="flex" :class="end ? 'justify-end' : 'justify-center'">
      <img :class="end ? '-mt-10' : ''" :src="`img/${img3}.svg`" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  props: ['h2', 'p1', 'p2', 'p3', 'img1', 'img2', 'img3', 'end'],
}
</script>

<style scoped>
.title {
  width: 280px;
}
.item {
  margin-right: 19px;
}
img {
  width: 270px;
  height: 270px;
  z-index: 9;
}
.mb-6rem {
  margin-bottom: -6rem;
}
.mr-6rem {
  margin-right: 62px;
}
.-mb-5rem {
  margin-bottom: -5rem;
}
.-mt-2rem {
  margin-top: -2.8rem;
}
.ml-4rem {
  margin-left: 4rem;
}
.ml-3rem {
  margin-left: 35px;
}
h2 {
  letter-spacing: 0px;
  font-size: 25px;
  font-weight: 600;
  color: #4a5568;
}
.number {
  letter-spacing: 0px;
  font-size: 150px;
  color: #718096;
  z-index: 99;
  height: 11rem;
}
.number-container {
  border-radius: 555rem;
  background: #f7fafc88 0% 0% no-repeat padding-box;

  margin-left: -4rem;
  flex-shrink: 0;
}
.item2 {
  padding-top: 3rem;
  background: transparent linear-gradient(134deg, #e6fffa 0%, #ebf4ff 100%) 0%
    0% no-repeat padding-box;
}
.p-1 {
  width: 100%;
  margin-left: -4rem;
  z-index: 9;
}
p {
  letter-spacing: 0.47px;
  color: #718096;
  font-size: 15.75px;
}
</style>
