<script>
import MyCal from "../views/MyCal.vue";
import MyPin from "../views/PinBoard.vue";
import MyToDo from "../views/ToDo.vue";

export default {
  name: "MainPage",
  components: {
    MyCal,
    MyPin,
    MyToDo,
  },
  data: function () {
    return {};
  },
  created: function () {},

  methods: {},
};
</script>

<template>
<div>
  <!-- <router-link class="spacing" to="/calendar">Calendario</router-link> -->
 <div style="height:100%;float:left">
   <sui-menu
    is="sui-sidebar"
    id="docs-menu"

    vertical="true"
    animation="overlay"
    :visible="true"
  >
   
    <sui-menu-item>
   
      <sui-menu-menu>
        <router-link is="sui-menu-item" to="/calendar">Calendario</router-link>
        <router-link is="sui-menu-item" to="/pinboard"> PinBoard </router-link>
        <router-link is="sui-menu-item" to="/todo"> To Do List </router-link>
      </sui-menu-menu>
    </sui-menu-item>
  </sui-menu>
  </div>
  <div style="height:100%;float:right"><router-view></router-view></div>
  </div> 
  
</template>

<style lang='css'>
</style>


