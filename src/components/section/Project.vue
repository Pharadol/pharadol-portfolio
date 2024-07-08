<script setup>
import Card from "../Card.vue";
import {projectList} from "../../assets/data/projectsLists"

const pathImg = "../src/assets/images/projects";
const workshopList = [
  {
    title: "Sawang",
    link: "https://www.youtube.com",
    thumbnail: `${pathImg}/Sawang.png`,
  },
  {
    title: "Sawang",
    link: "https://www.youtube.com",
    thumbnail: `https://img5.pic.in.th/file/secure-sv1/Sawang.png`,
  },
  {
    title: "Image Slider",
    link: "https://www.youtube.com",
    thumbnail: `https://img2.pic.in.th/pic/ImageSlider.png`,
  },
  {
    title: "Dek-D Internship",
    link: "https://www.youtube.com",
    thumbnail: `${pathImg}/`,
    view: "View",
    isNoneSourceCode: true,
  },
  {
    title: "Card Matching Game",
    link: "https://www.youtube.com",
    thumbnail: `${pathImg}/CardMatchingGame.png`,
  },
  {
    title: "Expense Tracker React",
    link: "https://www.youtube.com",
    thumbnail: `${pathImg}/ExpenseTrackerReact.png`,
  },
  {
    title: "Booking Movie Ticket",
    link: "https://www.youtube.com",
    thumbnail: `https://img5.pic.in.th/file/secure-sv1/BookingMovieTicket.png`,
  },
  {
    title: "Calculator",
    link: "https://www.youtube.com",
    thumbnail: `https://img5.pic.in.th/file/secure-sv1/calculator146edb0d5c48bc2e.png`,
  },
  {
    title: "Coundown to New Year",
    link: "https://www.youtube.com",
    thumbnail: `https://img2.pic.in.th/pic/coundown-new-yeard36a50d015ecf778.png`,
  },
  {
    title: "Currency Converter",
    link: "https://www.youtube.com",
    thumbnail: `https://img5.pic.in.th/file/secure-sv1/currency-converter.png`,
  },
  {
    title: "Theme Switcher JS",
    link: "https://www.youtube.com",
    thumbnail: `https://img5.pic.in.th/file/secure-sv1/theme-switcher-js.png`,
  },
  {
    title: "Music Player",
    link: "https://www.youtube.com",
    thumbnail: `https://img2.pic.in.th/pic/music-player.png`,
  },
  {
    title: "Note App",
    link: "https://www.youtube.com",
    thumbnail: `https://img2.pic.in.th/pic/Screenshot-2024-07-08-161042.png`,
  },
  {
    title: "Income Expense Tracker",
    link: "https://www.youtube.com",
    thumbnail: `https://img2.pic.in.th/pic/income-expense-tracker.png`,
  },
  {
    title: "Speed Typing Game",
    link: "https://www.youtube.com",
    thumbnail: `https://img2.pic.in.th/pic/speed-typing-game.png`,
  },
  {
    title: "Reveal Text On Scroll",
    link: "https://www.youtube.com",
    thumbnail: `https://img5.pic.in.th/file/secure-sv1/reveal-text-on-scroll.png`,
  },
];
</script>

<template>
  <section id="project">
    <div class="main">
      <h2>PROJECT & WORKSHOP</h2>
      <img src="/src/assets/images/projects/CardMatchingGame.png" alt="">
      <div class="project-list">
        <Card v-for="item in projectList" :key="item.title" :item="item" />
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  @apply min-h-[500px] bg-zinc-900 px-4 pb-20;
  .main {
    @apply container mx-auto text-zinc-100 max-w-[1220px] py-12;
    h2 {
      @apply text-2xl md:text-4xl font-semibold mb-12 sm:mb-16;
    }
    .project-list {
      @apply grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 md:gap-10;
    }
  }
}
</style>