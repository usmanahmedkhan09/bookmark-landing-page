<template>
  <header class="header" :class="isOpen ? 'close' : ''">
    <div class="header__logo">
      <LogoIcon />
    </div>
    <nav>
      <ul role="list">
        <li>Features</li>
        <li>Pricing</li>
        <li>Contact</li>
        <li>
          <button class="btn">Login</button>
        </li>
      </ul>
    </nav>
    <iconMenuVue @click="isOpen = !isOpen" class="header__menu" />
  </header>
  <sidebarVue @change="isOpen = false" :class="isOpen ? 'open' : ''" />
</template>
<script lang="ts">
import { defineComponent, ref } from "vue";
import LogoIcon from "../icons/logoIcon.vue";
import iconMenuVue from "../icons/icon-menu.vue";
import sidebarVue from "./sidebar.vue";

export default defineComponent({
  components: { LogoIcon, iconMenuVue, sidebarVue },
  setup() {
    const isOpen = ref(false);
    return { isOpen };
  },
});
</script>
