<template>
  <header class="header">
    <div class="logo">
      <LogoIcon />
    </div>
    <nav>
      <ul>
        <li>Features</li>
        <li>Pricing</li>
        <li>Contact</li>
        <li>
          <button class="btn">Login</button>
        </li>
      </ul>
    </nav>
  </header>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import LogoIcon from "../icons/logoIcon.vue";

export default defineComponent({
  components: { LogoIcon },
  setup() {
    return {};
  },
});
</script>
