<template>
  <div class="inner-body">
    <b-container class="inner-menu">
      <div class="bv">
        <div  v-for="(menu, index) in menus" v-bind:key="index" text-wrap="false">
          <button variant="outline-primary sm">{{menu}}</button>
        </div>
      </div>
    </b-container>

    <div class="text-center" v-for="(card, index) in cards" v-bind:key="index">
      <div class="card-body">
        <h5 class="card-title">{{card.name}}</h5>
        <p class="card-text">{{card.description}}</p>
        <a href="#" class="btn btn-primary">{{card.date}}</a>
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
          date: "09-01-2019",
          category: "child",
          description:"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley ",
          rating: 5,
          comments: 5
        },
        {
          name: "Victor RAJI",
          date: "10-01-2019",
          category: "men",
          description: "of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in ",
          rating: 1,
          comments: 2
        },
        {
          name: "Logan SHOLA",
          date: "12-01-2019",
          category: "women",
          description: "the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
          rating: 1,
          comments: 2
        },
        {
          name: "Mr.SANUSI",
          date: "14-01-2019",
          category: "men",
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
  height: 80%;

}
.inner-menu {
  width: 100%;
  margin: 0 auto;
 
}
.bv {
  overflow-x: scroll;
  display: flex;
  height:70px;
   margin-bottom: 22px;
    margin-left: 25px;
    margin-right: 40px;
     margin-top: 22px
  
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


  border-radius: 30px;
  position: relative;
  text-align: center;
  margin-left: 30px;
  border-width: 1px;
  border-style: solid;
  border-color: #1a77bb;
  color: #1a77bb;
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
  width: 150px;
  height: 23px;
  display: block;
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
