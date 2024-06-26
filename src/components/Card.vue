<script setup>
const props = defineProps({
  item: {
    type: Object,
    required: true,
  },
});

const onClickImg = (link) => {
  window.open(link, "_blank");
};
</script>

<template>
  <article>
    <div class="thumb-wrapper" @click="onClickImg(item.link)">
      <img :src="item.thumbnail" :alt="item.title" />
    </div>
    <div class="cart-content">
      <h3>{{ item.title }}</h3>
      <div>
        <a :href="item.link" target="_blank">{{ item.view ? item.view : "Website" }}</a>
        <hr v-show="!item.isNoneSourceCode" />
        <a v-show="!item.isNoneSourceCode" href="#" target="_blank">Github</a>
      </div>
    </div>
  </article>
</template>

<style scoped>
article {
  @apply overflow-hidden;
  .thumb-wrapper {
    @apply bg-zinc-700 h-[285px] cursor-pointer rounded-t-md overflow-hidden;
    img {
      @apply w-full h-full object-cover rounded-t-md transition-all duration-300 ease-out;
    }
  }
  .cart-content {
    @apply bg-[#1d1d1f] rounded-b-md p-8;
    h3 {
      @apply text-xl mb-1 font-semibold;
    }
    div {
      @apply flex items-center text-zinc-400 gap-x-2;
      hr {
        @apply border-zinc-300 w-6;
      }
      a:hover {
        @apply text-zinc-100 duration-200;
      }
    }
  }
  &:hover {
    .thumb-wrapper img {
      @apply scale-105;
    }
  }
}
</style>
