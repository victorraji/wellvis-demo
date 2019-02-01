<template>
  <div class="profile">
    <b-nav vertical class="w-25">
  <b-nav-item active>Home</b-nav-item>
  <b-nav-item>Profile</b-nav-item>
  <b-nav-item text-wrap="false" >Support Group</b-nav-item>
</b-nav>
    <!--<nav>
      <b-list-group class="nav-item">
  <b-list-group-item variant="secondary" href="#some-link">Home</b-list-group-item>
  <b-list-group-item href="#">Profile</b-list-group-item>
  <b-list-group-item href="#"> Group</b-list-group-item>
</b-list-group>
  </nav>-->

  </div>
</template>

<script>
import { mapGetters } from 'vuex'

import 'material-icons/iconfont/material-icons.css';
export default {
 data(){

return{

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
   .Profile {
  width: 100%; /* only for demonstration, should be removed */
  background:#ffff;

}

</style>
