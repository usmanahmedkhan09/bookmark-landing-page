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
  </main>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import HeroIcon from "../icons/heroIcon.vue";

export default defineComponent({
  components: {
    HeroIcon,
  },
  setup() {
    return {};
  },
});
</script>
