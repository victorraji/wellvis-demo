<template>
  <div class="hello">
      <navbar1/>
      <navbar2/>
       <div class="vl">    
       </div>
    
      <Profile/>
      <Cards/>
      </div>
 

</template>

<script>
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";
import Profile from "@/components/Profile.vue";
import Cards from "@/components/Cards.vue";
import Navbar1 from "@/components/Navbar1.vue";
import Navbar2 from "@/components/Navbar2.vue";


import { mapState } from "vuex";

import "material-icons/iconfont/material-icons.css";

export default {
  data() {
    return {
      namee: "victor"
    };
  },
  name: "HelloWorld",
  components: {
    Profile,
    Cards,
    Navbar1,
    Navbar2,
  
  },
  computed: { ...mapState(["title", "links"]) }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
html,
#app,
.home {
  height: 100%;
}
body {
  background-color: #f4f4f4;
  margin: 0;
  height: 100%;
}
.hello {
  display: grid;
  width: 100%;
  grid-template-columns: 20% 80%;
  grid-template-rows: 10% 80%;
  height: 100%;
}

.vl {
  border-left: 1px solid gainsboro;
  height: 1000px;
  position: absolute;
  left: 20%;
  top: 0;
}


</style>