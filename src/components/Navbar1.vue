<template>
 <div>
    <b-navbar toggleable type="primary" variant="primary">
        <b-navbar-toggle target="nav_text_collapse"></b-navbar-toggle>
        <b-navbar-brand></b-navbar-brand>
        <b-collapse is-nav id="nav_text_collapse">
            <b-navbar-nav>
                <b-nav-text>.</b-nav-text>
            </b-navbar-nav>
        </b-collapse>
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
