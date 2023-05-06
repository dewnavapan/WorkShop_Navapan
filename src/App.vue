<template>
  <div id="app">
    <v-bottom-navigation v-model="value">
      <v-btn value="Home" @click="goToHome()">
        <router-link to="/home">HOME</router-link>
      </v-btn>

      <v-btn value="profile" @click="goToPage1()">
        <router-link to="/profile">PROFILE</router-link>
      </v-btn>

      <v-btn value="contact" @click="goToPage2()">
        <router-link to="/contact">CONTACT</router-link>
      </v-btn>

      <v-btn value="project" @click="goToPage3()">
        <router-link to="/project">PROJECT</router-link>
      </v-btn>
    </v-bottom-navigation>

    <router-view />
  </div>
</template>

   

<script>
export default {
  name: "App",
  data: () => ({}),
  methods: {
    goToHome() {
      this.$router.push("/");
    },
    goToPage1() {
      this.$router.push("/profile");
    },
    goToPage2() {
      this.$router.push("/contact");
    },
    goToPage3() {
      this.$router.push("/project");
    },
  },
};
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.router-link-exact-active {
  color: blue;
}
.v-bottom-navigation {
  background-color: black;
}
</style>
