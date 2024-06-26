<template>
  <section id="home" class="bg-gray-400">
    <div>
      <h1>PHARADOL NUANPHIN</h1>
      <p>FRONT END DEVELOPER</p>
    </div>
  </section>
</template>

<style scoped>
section {
  @apply bg-no-repeat bg-cover bg-center flex justify-center items-center h-[600px] sm:h-[800px] lg:h-[850px] 4xl:h-[1350px] ;
  background-image: linear-gradient(180deg, #00000012 60%, #18181b 90%,#18181b 100%),
    url("../../assets/images/bg.jpg");
  div {
    @apply text-white text-center;
    h1 {
      @apply text-3xl sm:text-4xl md:text-6xl font-bold text-center mb-6 md:mb-10;
      text-shadow: 0px 0px 10px #000;
    }
    p {
      @apply text-lg sm:text-2xl md:text-4xl text-center;
      text-shadow: 0px 0px 10px #000;
    }
  }
}
</style>
