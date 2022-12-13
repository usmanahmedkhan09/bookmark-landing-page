<template>
  <div class="extension__card" :class="extension.name.toLowerCase()">
    <div class="extension__card--header">
      <img :src="getImageUrl(extension.name)" alt="" />
    </div>
    <div class="extension__card--body">
      <p class="extension__card--body--title">Add to {{ extension.name }}</p>
      <p class="extension__card--body--subtitle">
        Minimum version {{ extension.version }}
      </p>
      <div class="extension__card--seperator">
        <img src="../../../assets/images/bg-dots.svg" alt="" />
      </div>
    </div>
    <div class="extension__card--footer">
      <button class="btn">Add & Install Extension</button>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: ["extension"],
  setup() {
    const getImageUrl = (name: any) => {
      return new URL(
        `../../../assets/images/logo-${name.toLowerCase()}.svg`,
        import.meta.url
      ).href;
    };
    return {
      getImageUrl,
    };
  },
});
</script>
