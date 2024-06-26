<script setup></script>

<template>
  <footer id="contact">
    <div class="content-wrapper">
      <h3>Portfolio</h3>
      <p>Pharadol Nuanphin | Front end developer</p>
      <p>Gmail: <a href="mailto:pharadol.n@gmail.com">pharadol.n@gmail.com</a> | Call : 0956143323</p>
      <hr />
      <p>Website developed to showcase my portfolio of activities.</p>
      <span>© copyright Portfolio 2024 All Rights Reserved</span>
    </div>
  </footer>
</template>

<style scoped>
footer {
  @apply bg-[#1d1d1f] py-20 text-zinc-100 px-4;
  .content-wrapper {
    @apply container mx-auto max-w-[1220px] flex flex-col items-center;
    h3 {
      @apply text-2xl font-bold mb-2;
    }
    p {
      @apply text-zinc-200 text-center;
      a {
        @apply hover:text-blue-300;
      }
    }
    hr {
      @apply border-zinc-400 w-full my-1;
    }
    span {
      @apply text-zinc-500;
    }
  }
}
</style>
