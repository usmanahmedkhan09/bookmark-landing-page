<template>
  <div class="content__features--bookmarkTab">
    <div class="bookmarkTab__image">
      <div class="image__wrapper">
        <img
          class="searching"
          src="../../../assets/images/illustration-features-tab-2.svg"
          alt=""
        />
      </div>
    </div>
    <div class="bookmarkTab__details">
      <h2 class="bookmarkTab__details--title">Intelligent search</h2>
      <p class="bookmarkTab__details--description">
        Our powerfull search feature will help you to find saved <br />
        sites in no time at all.No need to trawl through all of <br />
        your bookmarks
      </p>
      <button class="btn">More Info</button>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  setup() {
    return {};
  },
});
</script>
