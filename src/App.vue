<template>
  <div id="app">
    <component :is="layout">
        <transition name="fade" mode="out-in">
            <router-view></router-view>
        </transition>
    </component>
  </div>
</template>

<script>
import axios from 'axios';

 


// нужный вариант 

// axios.post("https://dev-api.ringapp.me/auth", my_data, {
       //   headers: {
       //     'Authorization': 'Bearer' + 'Your Bearer Pssword',
        //    "Content-Type": "application/json",
        //    }
       //     })
        //    .then(function(response) {
       //         console.log(response=>data.token);
         //   })
       //     .catch(function (error) {
        //        console.log(error);
        //   });
   

  const default_layout = "default";

  export default {
    computed: {
      layout() {
        return (this.$route.meta.layout || default_layout) + '-layout';
      }
    }
  }

    
  
</script>

<style lang="scss">
  @import "assets/base.scss";
</style>
