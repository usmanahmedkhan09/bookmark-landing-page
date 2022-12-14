<template>
  <headerVue />
  <contentVue />
  <footerVue />
</template>
<script lang="ts">
import { defineComponent } from "vue";
import headerVue from "./header.vue";
import contentVue from "./content.vue";
import footerVue from "./footer.vue";

export default defineComponent({
  components: {
    headerVue,
    contentVue,
    footerVue,
  },
  setup() {
    return {};
  },
});
</script>
