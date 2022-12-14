<template>
  <div class="accordion card">
    <div class="header" @click="isOpen = !isOpen">
      <p>{{ question.title }}</p>
      <div class="header_icon">
        <iconArrowVue :class="!isOpen ? 'open__svg' : 'close__svg'" />
      </div>
    </div>
    <div class="accordion--content" :class="isOpen ? 'open' : ''">
      {{ question.answer }}
      <!-- <slot></slot> -->
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref } from "vue";
import iconArrowVue from "./icons/icon-arrow.vue";

export default defineComponent({
  components: { iconArrowVue },
  props: ["question"],
  setup(props) {
    const isOpen = ref(false);
    return { isOpen };
  },
});
</script>
