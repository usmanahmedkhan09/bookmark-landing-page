<template>
  <div class="header__sidebar">
    <div class="header__sidebar--menu">
      <img src="../../assets/images/logo-bookmark.svg" alt="" />
      <iconCrossVue @click="$emit('change')" class="" />
    </div>
    <ul class="header__sidebar--list">
      <li>features</li>
      <li>pricing</li>
      <li>contact</li>
      <li>
        <button class="btn">login</button>
      </li>
    </ul>
    <div class="header__sidebar--icons">
      <iconFacebookVue />
      <iconTwitterVue />
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import iconCrossVue from "../icons/icon-cross.vue";
import iconFacebookVue from "../icons/icon-facebook.vue";
import iconTwitterVue from "../icons/icon-twitter.vue";

export default defineComponent({
  components: { iconCrossVue, iconFacebookVue, iconTwitterVue },
  setup() {
    return {};
  },
});
</script>
