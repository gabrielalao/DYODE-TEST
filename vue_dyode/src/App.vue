<template>
  <div id="app">
    <router-view name="header"></router-view>
    <main>
      <fade-transition origin="center" mode="out-in" :duration="250">
        <router-view />
      </fade-transition>
    </main>
    <router-view name="footer"></router-view>
  </div>
</template>
<script>
import { FadeTransition } from "vue2-transitions";

export default {
  components: {
    FadeTransition,
  },
};
</script>
<style>
@font-face {
  font-family: "Pacifico";
  src: local("Pacifico"),
   url(/fonts/Pacifico_Font/Pacifico.ttf) format("truetype");
}
@font-face {
  font-family: "Lato-Light";
  src: local("Lato-Light"),
   url(/fonts/Lato/Lato-Light.ttf) format("truetype");
}
@font-face {
  font-family: "Lato-Regular";
  src: local("Lato-Regular"),
   url(/fonts/Lato/Lato-Regular.ttf) format("truetype");
}
@font-face {
  font-family: "Lato-Bold";
  src: local("Lato-Bold"),
   url(/fonts/Lato/Lato-Bold.ttf) format("truetype");
}
</style>