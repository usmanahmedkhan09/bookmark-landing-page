<template>
  <main class="content">
    <section class="content__intro">
      <div class="content__intro--details">
        <p class="content__intro--title">
          A Simple Bookmark <span> Manager </span>
        </p>
        <p class="content__intro--description">
          A clean and simple interface to organize your favourite <br />
          websites.Open a new browser tab and see your sites load <br />
          intantly.Try it for free.
        </p>
        <div class="content__intro--buttons">
          <button class="btn">Get it on Chrome</button>
          <button class="btn">Get it on Firefox</button>
        </div>
      </div>
      <div class="content__intro--image">
        <div class="content__intro--design">
          <HeroIcon class="content__intro--design--svg" />
        </div>
      </div>
    </section>
    <section class="content__features">
      <div class="content__header">
        <p class="content__header--title">Features</p>
        <p class="content__header--description">
          Our aim is to make it quick and easy for you to access your <br />
          favourite websites.Your Bookmarks sync between your devices <br />
          so you can access them on the go
        </p>
        <ul class="content__features--tabs">
          <li class="active">Simple Bookmarking</li>
          <li>Speedy Searching</li>
          <li>Easy Sharing</li>
        </ul>
      </div>
      <component :is="activeTab"></component>
    </section>
  </main>
</template>
<script lang="ts">
import { defineComponent, ref } from "vue";
import HeroIcon from "../icons/heroIcon.vue";
import BookMark from "./reusable/bookmark.vue";

export default defineComponent({
  components: {
    HeroIcon,
    BookMark,
  },
  setup() {
    const activeTab = ref(BookMark);
    return { activeTab };
  },
});
</script>
