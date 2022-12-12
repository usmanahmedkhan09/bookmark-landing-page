<template>
  <headerVue />
  <contentVue />
</template>
<script lang="ts">
import { defineComponent } from "vue";
import headerVue from "./header.vue";
import contentVue from "./content.vue";

export default defineComponent({
  components: {
    headerVue,
    contentVue,
  },
  setup() {
    return {};
  },
});
</script>
