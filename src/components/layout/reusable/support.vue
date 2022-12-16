<template>
  <p class="content__support--title">35.000+ already Joined</p>
  <p class="content__support--subTitle">
    Stay up-to-date with what <br />
    we're doing
  </p>
  <div class="content__support--contact">
    <div class="input__wrapper" :class="error.state ? 'error' : ''">
      <input
        v-model="email"
        type="text"
        placeholder="Enter your email address"
        @keypress="resetState()"
      />
      <span v-if="error.state"> {{ error.message }}</span>
      <img
        v-if="error.state"
        class=""
        src="../../../assets/images/icon-error.svg"
        alt=""
      />
    </div>
    <button class="btn" @click="validateEmail()">Contact Us</button>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  setup() {
    const email = ref("");

    let error = ref({
      message: "",
      state: false,
    });

    const validateEmail = () => {
      if (email.value.length > 0) {
        if (
          String(email.value)
            .toLowerCase()
            .match(
              /^([A-Za-z0-9_\-\.])+\@(?!(?:[A-Za-z0-9_\-\.]+\.)?([A-Za-z]{2,4})\.\2)([A-Za-z0-9_\-\.])+\.([A-Za-z]{2,4})$/
            )
          // .match(
          //     /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
          // )
        ) {
          return "";
        } else {
          error.value.message = "Whoops, make sure it's an email";
          error.value.state = true;
        }
      } else {
        error.value.message = "Email is required.";
        error.value.state = true;
      }
    };

    const resetState = () => {
      error.value.state = false;
      error.value.message = "";
    };

    return { email, validateEmail, error, resetState };
  },
});
</script>
