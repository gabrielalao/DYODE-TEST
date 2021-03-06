<template>
  <nav
    class="navbar"
    :class="[
            {'navbar-expand-lg': expand},
            {[`navbar-${effect}`]: effect},
            {'navbar-transparent': transparent},
            {[`bg-${type}`]: type},
            {'rounded': round}
         ]"
  >
    <div class="container">
      <slot name="container-pre"></slot>
      <navbar-toggle-button
        :toggled="toggled"
        :target="contentId"
        @click.native.stop="toggled = !toggled"
      ></navbar-toggle-button>

      <div
        class="collapse navbar-collapse"
        :class="{show: toggled}"
        :id="contentId"
        v-click-outside="closeMenu"
      >
        <div class="navbar-collapse-header">
          <slot name="content-header" :close-menu="closeMenu"></slot>
        </div>
        <slot :close-menu="closeMenu"></slot>
      </div>

      <slot name="container-after">
        <div class="mobile-menu">
        <router-link slot="content-header" class="navbar-brand mr-lg-5" to="/">
          <img src="img/img/Logo.png" alt="logo" />
        </router-link>
        </div>
      </slot>
      <slot name="container-last">
        <div class="mobile-menu">
        <router-link slot="content-header" class="navbar-brand mr-lg-5" to="/">
          <img src="img/img/Group 9.png" alt="logo" />
        </router-link>
        </div>
      </slot>

    </div>
  </nav>
</template>
<script>
import { FadeTransition } from "vue2-transitions";
import NavbarToggleButton from "./NavbarToggleButton";

export default {
  name: "base-nav",
  components: {
    FadeTransition,
    NavbarToggleButton,
  },
  props: {
    type: {
      type: String,
      default: "primary",
      description: "Navbar type (e.g default, primary etc)",
    },
    title: {
      type: String,
      default: "",
      description: "Title of navbar",
    },
    contentId: {
      type: [String, Number],
      default: Math.random().toString(),
      description:
        "Explicit id for the menu. By default it's a generated random number",
    },
    effect: {
      type: String,
      default: "dark",
      description: "Effect of the navbar (light|dark)",
    },
    round: {
      type: Boolean,
      default: false,
      description: "Whether nav has rounded corners",
    },
    transparent: {
      type: Boolean,
      default: false,
      description: "Whether navbar is transparent",
    },
    expand: {
      type: Boolean,
      default: false,
      description: "Whether navbar should contain `navbar-expand-lg` class",
    },
  },
  data() {
    return {
      toggled: false,
    };
  },
  methods: {
    onTitleClick(evt) {
      this.$emit("title-click", evt);
    },
    closeMenu() {
      this.toggled = false;
    },
  },
};
</script>
<style>
</style>
