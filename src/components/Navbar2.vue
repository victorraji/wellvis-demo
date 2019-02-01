<template>
<div class="right">
     
      <b-navbar toggleable="md" type="dark" variant="primary">
        <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

        <b-navbar-brand href="#">Feeds</b-navbar-brand>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" type="text" placeholder="Search"/>
            <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
          </b-nav-form>
        </b-navbar-nav>
      </b-navbar>

     
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
  width: 100%; /* only for demonstration, should be removed */
  background:#ffff;

}
.nav-item{
width: 99%;
border-radius: 0%
}

</style>
