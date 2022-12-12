<template>
  <div class="content__features--bookmarkTab">
    <div class="bookmarkTab__image">
      <div class="image__wrapper">
        <!-- <tabOneIcon class="image" /> -->
        <img
          class="image"
          src="../../../assets/images/illustration-features-tab-1.svg"
          alt=""
        />
      </div>
    </div>
    <div class="bookmarkTab__details">
      <h2 class="bookmarkTab__details--title">Bookmark in one click</h2>
      <p class="bookmarkTab__details--description">
        Organize your bookmarks however you like.Our <br />simple drag-n-drop
        inteface gives you complete <br />
        control over how you manage your favourite sites.
      </p>
      <button class="btn">More Info</button>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import tabOneIcon from "@/components/icons/tab-one.vue";

export default defineComponent({
  components: { tabOneIcon },
  setup() {
    return {};
  },
});
</script>
