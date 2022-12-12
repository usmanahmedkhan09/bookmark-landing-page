<template>
  <headerVue />
</template>
<script lang="ts">
import { defineComponent } from "vue";
import headerVue from "./header.vue";

export default defineComponent({
  components: {
    headerVue,
  },
  setup() {
    return {};
  },
});
</script>
