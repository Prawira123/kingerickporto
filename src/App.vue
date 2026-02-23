<template>
  <div class="w-full h-screen relative">
    <div class="sticky lg:top-[30px] top-[10px] z-10">
      <Nav/>
    </div>
    <div class="z-0 absolute top-0 left-0 w-full h-full">
      <div class="aurora-container ">
      <Aurora
        :color-stops="['#7cff67', '#171D22', '#7cff67']"
        :amplitude="1.0"
        :blend="0.5"
        :speed="1.0"
        :intensity="1.0"
        class="w-full h-full"
        />
        <Hero/>
      </div>
    </div>
  </div>
  <div class="py-[400px]"></div>
  
  <GradualBlur
    target="page"
    position="bottom"
    height="6rem"
    :strength="2"
    :divCount="5"
    curve="bezier"
    :exponential="true"
    :opacity="1"
  />
</template>

<script setup lang="ts">
  import Aurora from "./components/Aurora.vue";
  import Nav from "./components/nav.vue";
  import GradualBlur from "./components/GradualBlur.vue";
  import Hero from "./components/hero.vue"

</script>

<style scoped>
  .aurora-container {
    width: 100%;
    height: 100%;
    position: relative;
    overflow: hidden;
  }
</style>