<template>
  <v-app>
    <Navbar/>
    <div style="background-color: black">
      <v-container>
        <div width="100%" style="text-align:center;">
        <img width="100%" style="max-height:280px; max-width:852px" class="mt-4"  src="./images/logo_lg.jpg">
        </div>
      </v-container>
    </div>

    <router-view style="margin-bottom: 60px"></router-view>

    <Footer/>
  </v-app>
</template>


<script>
import Navbar from "@/components/Navbar";
import Footer from "@/components/Footer";

export default {
  name: "App",
  components: {
    Navbar,
    Footer
  },
  data() {
    return {
      //
    };
  }
};
</script>
