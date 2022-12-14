<template>
  <div class="footer">
    <ul class="footer__list">
      <li><logoIconVue /></li>
      <li>Features</li>
      <li>Pricing</li>
      <li>Contact</li>
    </ul>
    <div class="footer__icons">
      <iconFacebookVue />
      <iconTwitterVue />
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import logoIconVue from "../icons/logoIcon.vue";
import iconFacebookVue from "../icons/icon-facebook.vue";
import iconTwitterVue from "../icons/icon-twitter.vue";

export default defineComponent({
  components: { logoIconVue, iconFacebookVue, iconTwitterVue },
  setup() {
    return {};
  },
});
</script>
