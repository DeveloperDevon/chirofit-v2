<template>
  <nav>
    <v-toolbar flat app color="black">
      <v-toolbar-side-icon class="grey--text hidden-sm-and-up" @click.native.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-tabs class="hidden-xs-only" color="black">
        <v-tab flat v-for="link in links" :key="link.text" :to="link.route" style="color: white;">
          <!-- <v-icon>{{link.icon}}</v-icon> -->
          {{link.text}}
        </v-tab>
      </v-tabs>
      <v-spacer></v-spacer>
      <ul
        v-for="link in socialMediaLink"
        :key="link.url"
        right
        hide-slider
        color="black"
      >
        <li>
          <a :href="link.url">
            <i :class="link.icon"></i>
          </a>
        </li>
      </ul>
    </v-toolbar>

    <v-navigation-drawer v-model="drawer" app class="primary">
      <v-list>
        <v-list-tile v-for="link in links" :key="link.text" router :to="link.route">
          <v-list-tile-action>
            <v-icon class="white--text">{{ link.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title class="white--text">{{ link.text }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>



<script>
export default {
  data() {
    return {
      drawer: false,
      links: [
        { icon: "home", text: "Home", route: "/" },
        { icon: "people", text: "Services", route: "/services" },
        { icon: "business", text: "Contact", route: "/contact" },
        { icon: "info", text: "About Us", route: "/about" }
      ],
      socialMediaLink: [
        {
          url: "https://www.facebook.com/chirofitroseville",
          icon: "fab fa-facebook-square fa-2x"
        },
        {
          url: "https://www.yelp.com/biz/chirofit-roseville-roseville",
          icon: "fab fa-yelp fa-2x"
        }
      ]
    };
  }
};
</script>
