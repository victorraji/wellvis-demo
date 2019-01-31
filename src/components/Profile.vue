<template>
  <div class="profile">
    <nav>
      <b-list-group class="nav-item">
  <b-list-group-item variant="secondary" href="#some-link">Home</b-list-group-item>
  <b-list-group-item href="#" active>Profile</b-list-group-item>
  <b-list-group-item href="#">Suport Group</b-list-group-item>
</b-list-group>
  </nav>

  </div>
</template>

<script>
import { mapGetters } from 'vuex'

import 'material-icons/iconfont/material-icons.css';
export default {
 data(){

return{
menus:[
 " All","Trending","Childhealth","Pregnanacy",
 "Women's health","Mental health",
 "Infections","Nutrition","Fitness",  
 "Skincare","Baby Care","Dental Care",
 "Medicine","General Health"
]
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
</style>
