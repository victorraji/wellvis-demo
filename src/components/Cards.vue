<template>
     <div class="inner-cards">
      <b-card
        v-for="(card, index) in cards" v-bind:key="index"
        title="Anonymous"
        style="max-width: 20rem;"
        class="mb-2">
        <p class="card-text" >
          </p>
          <b-button href="#" variant="primary">Go somewhere</b-button>
      </b-card>
    </div>
</template>

<script>
import { mapGetters } from 'vuex'

import 'material-icons/iconfont/material-icons.css';
export default {
 data(){

  return{
    cards: [
      {
        name: "codegod",
        date: "12-01-2019",
        category: "women",
        description: "breast cancer",
        rating: 0,
        comments: 0
      },
      {
        name: "codegod",
        date: "12-01-2019",
        category: "women",
        description: "breast cancer",
        rating: 0,
        comments: 0
      },
      {
        name: "codegod",
        date: "12-01-2019",
        category: "women",
        description: "breast cancer",
        rating: 0,
        comments: 0
      },
      {
        name: "codegod",
        date: "12-01-2019",
        category: "women",
        description: "breast cancer",
        rating: 0,
        comments: 0
      }
    ],
  }

  },
  computed: {
    ...mapGetters([
      'countLinks'
    ]),
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
   nav {
  float: left;
  width: 20%;
  height: 700px; /* only for demonstration, should be removed */
  background:#ffff;
  padding:0
}
.nav-item{
width: 99%;
border-radius: 0%
}

.inner-cards {
  width: 500cm;
  margin: 0 auto;
}
</style>
