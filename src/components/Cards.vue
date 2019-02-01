<template>
  <div class="inner-body">
    <b-container class="inner-menu">
      <div class="bv">
        <div v-for="(menu, index) in menus" v-bind:key="index" text-wrap="false">
          <button variant="outline-primary sm">{{menu}}</button>
        </div>
      </div>
    </b-container>

    <div class="text-center" v-for="(card, index) in cards" v-bind:key="index">
      <div class="card-body">
        <h5 class="card-title">{{card.name}}</h5>
        <p class="card-text">{{card.description}}</p>
        <a href="#" class="btn btn-primary">{{}}/a>
      </div>
      <div class="card-footer text-muted">{{card.rating}}</div>
    </div>

    <hr>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
import "material-icons/iconfont/material-icons.css";
export default {
  data() {
    return {
      menus: [
        " All",
        "Trending",
        "Childhealth",
        "Pregnanacy",
        "Women's health",
        "Mental health",
        "Infections",
        "Nutrition`",
        "Fitness",
        "Skincare",
        "Baby Care",
        "Dental Care",
        "Medicine",
        "General Health"
      ],
      cards: [
        {
          name: "codegod",
          date: "12-01-2019",
          category: "women",
          description:"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley ",
          rating: 5,
          comments: 5
        },
        {
          name: "victor",
          date: "10-01-2019",
          category: "men",
          description: "penis enlargement",
          rating: 1,
          comments: 2
        },
        {
          name: "codegod",
          date: "12-01-2019",
          category: "women",
          description: "eye lkashesr",
          rating: 1,
          comments: 2
        },
        {
          name: "codegod",
          date: "12-01-2019",
          category: "child",
          description: "leg pain",
          rating: 3,
          comments: 17
        }
      ]
    };
  },
  computed: {
    ...mapGetters(["countLinks"])
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
b-container {
  height: 50%;
}
.inner-menu {
  width: 100%;
  margin: 0 auto;
}
.bv {
  overflow-x: scroll;
  display: flex;
}
[text-capitalize] {
  text-transform: capitalize !important;
}
button {
  border: 0;
  font-family: inherit;
  font-style: inherit;
  font-variant: inherit;
  line-height: 1;
  text-transform: none;
  cursor: pointer;
  -webkit-appearance: button;
  display: inline-block;

  border-radius: 30px;
  position: relative;
  text-align: center;
  margin-left: 50px;
  border-width: 1px;
  border-style: solid;
  border-color: #1a77bb;
  color: #1a77bb;
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
  width: 150px;
  height: 23px;
}
button:hover {
  background-color: gainsboro;
}
button:active {
  background-color: blue;
}
.text-center {
  width: 50%;
  margin: 0 auto;
  padding-top: 20px;
}
</style>
