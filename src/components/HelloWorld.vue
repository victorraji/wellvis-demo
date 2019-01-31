<template>
 <div class="hello">

   <div class="right">
     
 <!--
    <div class="left">
      <h1>{{ title }}</h1>

      
    </div>
    <div class="right">
      <stats />  < Add this 
    </div>
 -->
<b-navbar toggleable="md" type="dark" variant="info">

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
  <Profile/>
  <div class="vl"></div>

<b-container >
  <b-row>

    <b-col class="bv"
       v-for="(menu, index) in menus" v-bind:key="index">
     
       <b-button  variant="outline-primary sm">
          {{ menu}}
          </b-button >
        </b-col>
        </b-row>
</b-container>
<Cards/>
</div>
<!-- navbar-1.vue -->
  </div>

  
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
import Profile from '@/components/Profile.vue'
import Cards from '@/components/Cards.vue'

import { mapState } from 'vuex'

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
  name: 'HelloWorld',
 components:{
Profile,
Cards

 },
  computed: 
  { ...mapState([
      'title','links'
    ]),
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.left {
    padding: 10px;
    grid-area: left;
    background-color: #E9E9E9;
  }
 .vl {
  border-left: 1px solid gainsboro;
  height: 800px;
  position: absolute;
  left: 20%;
  margin-left: -3px;
  top: 0;
  }

  .bv{
display: flex;
overflow-x:scroll
  }
  b-container{
display: flex;
overflow-x:scroll
  }

</style>