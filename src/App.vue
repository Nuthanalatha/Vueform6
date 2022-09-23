<template>
  <nav-bar />
  <!-- <from-component @getFormDataFromLogin="getFormDataFromLogin" />
  <user-data :userFormData="userFormData" /> -->
  <vee-form />
</template>

<script>
// import FromComponent from "./components/FromComponent.vue";
// import NavBar from "./components/NavBar.vue";
// import UserData from "./components/UserData.vue";
import VeeForm from "./components/VeeForm.vue";
export default {
  name: "App",
  components: {
    // FromComponent,
    //  NavBar,
    // UserData,
    VeeForm,
  },
  data() {
    return {
      userFormData: [],
    };
  },
  methods: {
    getFormDataFromLogin(formData) {
      // console.log("formData in parent",formData);
      this.userFormData.push(formData);
      console.log("userFormData", this.userFormData);
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
  /* margin-top: 60px; */
}
</style>
