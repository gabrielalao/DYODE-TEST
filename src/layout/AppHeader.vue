<template>
  <header class="header-global" style="background: #10504F;">
     <div class="header-description">
        <span class="title">FREE SHIPPING ON ALL ORDERS OVER $75</span>
     </div>

    <base-nav class="navbar-main" transparent type effect="light" expand>
      <div class="row" slot="content-header" slot-scope="{closeMenu}">
        <div class="col-6 collapse-brand">
          <a href="https://demos.creative-tim.com/vue-argon-design-system/documentation/">
            <img src="img/img/Logo.png" />
          </a>
        </div>
        <div class="col-6 collapse-close">
          <close-button @click="closeMenu"></close-button>
        </div>
      </div>

      <ul class="navbar-nav navbar-nav-hover align-items-lg-center">
        <router-link class="navbar-brand mr-lg-5" to="/">
          <img src="img/img/Logo.png" alt="logo" />
        </router-link>
        <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
          <i class="ni ni-ui-04 d-lg-none"></i>
          <span class="nav-link-inner--text">Womens</span>
        </a>
        <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
          <i class="ni ni-collection d-lg-none"></i>
          <span class="nav-link-inner--text">Mens</span>
        </a>
        <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
          <i class="ni ni-collection d-lg-none"></i>
          <span class="nav-link-inner--text">Accessories</span>
        </a>
        <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
          <i class="ni ni-collection d-lg-none"></i>
          <span class="nav-link-inner--text">Sales</span>
        </a>
      </ul>
    </base-nav>
  </header>
</template>
<script>
import BaseNav from "@/components/BaseNav";
import BaseDropdown from "@/components/BaseDropdown";
import CloseButton from "@/components/CloseButton";

export default {
  components: {
    BaseNav,
    CloseButton,
    BaseDropdown,
  },
};
</script>
<style>
</style>
