<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";

const menuList = [
  {
    title: "Home",
    to: "home",
  },
  {
    title: "Project",
    to: "project",
  },
  {
    title: "Contact",
    to: "contact",
  },
];

const showNavbar = ref(true);
let lastScrollPosition = 0;

const onScroll = () => {
  const currentScrollPosition =
    window.scrollY || document.documentElement.scrollTop;
  if (currentScrollPosition < 0) return;
  showNavbar.value = currentScrollPosition < lastScrollPosition;
  lastScrollPosition = currentScrollPosition;
};

onMounted(() => {
  window.addEventListener("scroll", onScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener("scroll", onScroll);
});

const scrollToSection = (sectionId, offset = 0) => {
  const element = document.getElementById(sectionId);
  if (element) {
    const elementPosition =
      element.getBoundingClientRect().top + window.scrollY;
    const offsetPosition = elementPosition - offset;

    window.scrollTo({
      top: offsetPosition,
      behavior: "smooth",
    });
  }
};
</script>

<template>
  <nav :class="{ 'navbar--hidden': !showNavbar }">
    <div class="nav-content">
      <div class="logo">Portfolio</div>
      <ul>
        <li v-for="item in menuList" :key="item.title">
          <button @click="scrollToSection(item.to)">
            {{ item.title }}
          </button>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
nav {
  @apply navbar p-4 z-20 pb-9;
  background-image: linear-gradient(
    180deg,
    rgba(24, 24, 27, 1) 0%,
    rgba(24, 24, 27, 1) 60%,
    rgba(24, 24, 27, 0) 100%
  );
  .nav-content {
    @apply container mx-auto max-w-[1220px] flex justify-between items-center;
    .logo {
      @apply
      text-gray-100 font-semibold text-2xl;
    }
    ul {
      @apply text-gray-300 flex w-fit gap-5 sm:gap-12;
      li {
        button {
          @apply text-lg font-semibold;
          &:hover {
            @apply cursor-pointer underline text-gray-100;
          }
        }
      }
    }
  }
}
.navbar {
  @apply fixed top-0 w-full;
  transition: 0.3s all ease-out;
  transform: translate3d(0, 0, 0);
}

.navbar.navbar--hidden {
  transform: translate3d(0, -100%, 0);
}
</style>
