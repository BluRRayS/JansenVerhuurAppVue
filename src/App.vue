<template>
  <v-app class="grey lighten-4">
    <v-main>
      <NavBar />
      <v-content>
        <v-container>
          <transition name="fade">
            <router-view></router-view>
          </transition>
        </v-container>
      </v-content>
    </v-main>
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar";

export default {
  name: "App",

  components: {
    NavBar,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
.fade-enter-active, .fade-leave-active {
  transition: opacity .3s ease-in-out, transform .3s ease;
}
.fade-enter-active{
  transition-delay: .3s;
}

.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

.fade-enter-to, .fade-leave{
  opacity: 1;
}
</style>
