<template>
  <div class="home">
    <v-container>
    <h4 class="display-1 mt-3" style="text-align:center">Welcome to ChiroFit Roseville</h4>
    <h4 class="headline mb-3" style="text-align:center">Your Roseville Chiropractors</h4>
    <v-container>
    <p
      style="text-align:justify"
      class="subheader"
    >Dr. Josh Reichardt and Dr. Jon McHale both grew up in the Roseville/Sacramento area. Both attended Sierra College in Rocklin and were classmates at Life Chiropractic College West in Hayward, CA. For two years following graduation, Dr. Reichardt and Dr. McHale have gained valuable experience and learned cutting edge techniques through school, and their year long internship in the Life West Health Center and from working alongside top Chiropractors for the past two years.</p>
    </v-container>

    <v-container style="max-width:1137px">
      <v-carousel >
        <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src" ></v-carousel-item>
      </v-carousel>
    </v-container>
    <h4 class="display-1 mb-3" style="text-align:center">What Makes Us Different</h4>
    <v-container>
    <v-layout row wrap >
      <v-flex v-for="card in cards" :key="card.title" xs12 sm4>
        <v-container style="text-align: center">
          <v-card>
            <v-card-title class="headline" style="text-align: center">{{ card.title}}</v-card-title>
            <div>{{ card.body }}</div>
            <v-flex xs12>
              <v-card-actions>
                <v-btn style="width:100%" flat color="primary" :to="card.link">{{ card.linkText }}</v-btn>
              </v-card-actions>
            </v-flex>
          </v-card>
        </v-container>
      </v-flex>
    </v-layout>
    </v-container>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: "https://i.imgur.com/cu5jv85.jpg"
        },
        {
          src: "https://i.imgur.com/dzFuONS.jpg"
        },
        {
          src: "https://i.imgur.com/SERdB7n.jpg"
        },
        {
          src: "https://i.imgur.com/SE6QlbS.jpg"
        }
      ],
      cards: [
        {
          title: "Your well-being is our priority",
          body:
            "At your first visit to ChiroFit Roseville, Dr. Reichardt or Dr. McHale will explain how chiropractic care works and give you a full evaluation to see if our chiropractic solutions fit your needs.",
          linkText: "Services",
          link: "/services"
        },
        {
          title: "We're Experienced Doctors",
          body:
            "Dr. Reichardt worked and learned from Chiropractors in Lafayette with over 35 years experience and Dr. McHale worked with another Chiropractor in Roseville with over 30 years experience as well.",
          linkText: "About Us",
          link: "/about"
        },
        {
          title: "Passion to Help People",
          body:
            "Their passion to help people feel better and reach their maximum potential lead them to team up and start ChiroFit Roseville, where they can now help members of the community they grew up in.",
          linkText: "Contact Us",
          link: "/contact"
        }
      ]
    };
  }
};
</script>
