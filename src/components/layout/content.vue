<template>
  <main class="content">
    <section class="content__intro">
      <div class="content__intro--details">
        <p class="content__intro--title">
          A Simple Bookmark <br />
          Manager
        </p>
        <p class="content__intro--description">
          A clean and simple interface to organize your favourite <br />
          websites.Open a new browser tab and see your sites load <br />
          intantly.Try it for free.
        </p>
        <div class="content__intro--buttons">
          <button class="btn">Get it on Chrome</button>
          <button class="btn">Get it on Firefox</button>
        </div>
      </div>
      <div class="content__intro--image">
        <img src="../../assets/images/illustration-hero.svg" alt="" />
        <div class="bg"></div>
      </div>
    </section>
    <section class="content__features">
      <div class="content__header">
        <p class="content__header--title">Features</p>
        <p class="content__header--description">
          Our aim is to make it quick and easy for you to access your <br />
          favourite websites.Your Bookmarks sync between your devices <br />
          so you can access them on the go
        </p>
        <ul class="content__features--tabs">
          <li
            @click="activeTab = tab.value"
            :class="tab.value == activeTab ? 'active' : ''"
            v-for="(tab, index) in tabs"
            :key="index"
          >
            {{ tab.name }}
          </li>
        </ul>
      </div>
      <component :is="activeTab"></component>
    </section>
    <section class="content__extensions">
      <div class="content__extensions--header">
        <p class="content__extensions--header--title">Download the extension</p>
        <p class="content__extensions--header--description">
          We've got more brwoser in the pipeline.Please do let us know if <br />
          you've got a favourite you'd like us to prioritize. <br />
        </p>
      </div>
      <div class="cards__container">
        <extensionCard
          v-for="(extension, index) in extensioncrads"
          :extension="extension"
          :key="index"
        >
        </extensionCard>
      </div>
    </section>
    <section class="content__questions">
      <div class="content__questions--header">
        <p class="content__questions--header--title">
          Frequently Asked Questions
        </p>
        <p class="content__questions--header--description">
          Here are some of our FAQ's.if you have any other questions <br />
          you'd like answered please feel free to email us. <br />
        </p>
      </div>
      <div class="content__questions--accordian">
        <accordianVue
          :question="question"
          v-for="(question, index) in questions"
          :key="index"
        />
      </div>
      <div class="content__questions--button">
        <button class="btn">More Info</button>
      </div>
    </section>
    <section class="content__support">
      <supportVue />
    </section>
  </main>
</template>
<script lang="ts">
import { defineComponent, ref } from "vue";
import HeroIcon from "../icons/heroIcon.vue";
import BookMark from "./reusable/bookmark.vue";
import Searching from "./reusable/searching.vue";
import Sharing from "./reusable/sharing.vue";
import extensionCard from "./reusable/extension-card.vue";
import accordianVue from "../accordian.vue";
import supportVue from "./reusable/support.vue";
export default defineComponent({
  components: {
    HeroIcon,
    BookMark,
    Searching,
    Sharing,
    extensionCard,
    accordianVue,
    supportVue,
  },
  setup() {
    const tabs = ref([
      { name: "Simple Bookmarking", value: "BookMark" },
      { name: "Speedy Searching", value: "Searching" },
      { name: "Easy Sharing", value: "Sharing" },
    ]);
    const activeTab = ref("BookMark");

    const extensioncrads = ref([
      { name: "Chrome", version: "62" },
      { name: "FireFox", version: "55" },
      { name: "Opera", version: "46" },
    ]);

    const questions = ref([
      {
        title: "What is BookMark?",
        answer:
          "Lorem ipsum dolor sit amet consectetur adipisicing elit. A, impedit eaque Quia facere aut doloribus dolorem quasi laborum voluptatum, voluptate ex ipsa, a nam non obcaecati architecto sit totam temporibus?",
      },
      {
        title: "How can I request a new browser?",
        answer:
          "Lorem ipsum dolor sit amet consectetur adipisicing elit. A, impedit eaque Quia facere aut doloribus dolorem quasi laborum voluptatum, voluptate ex ipsa, a nam non obcaecati architecto sit totam temporibus?",
      },
      {
        title: "Is there a mobile app?",
        answer:
          "Lorem ipsum dolor sit amet consectetur adipisicing elit. A, impedit eaque Quia facere aut doloribus dolorem quasi laborum voluptatum, voluptate ex ipsa, a nam non obcaecati architecto sit totam temporibus?",
      },
      {
        title: "What about other Chromium browser?",
        answer:
          "Lorem ipsum dolor sit amet consectetur adipisicing elit. A, impedit eaque Quia facere aut doloribus dolorem quasi laborum voluptatum, voluptate ex ipsa, a nam non obcaecati architecto sit totam temporibus?",
      },
    ]);

    return { activeTab, tabs, extensioncrads, questions };
  },
});
</script>
