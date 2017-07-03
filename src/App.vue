<template>
  <div id="app">


    <header>
      <el-row :gutter="10" v-if="this.$route.name != 'home'">
        <el-col :span="3" :xs="5">
          <router-link to="/" class="site-logo">
            Search for the Stars
          </router-link>
        </el-col>
        <el-col :span="18">
          <search-form inline icon="search" size="76" />
        </el-col>
      </el-row>
    </header>
    <div class="main">

      <el-row>
        <el-col :span="21" :offset="3" :xs="{offset:0, span:24}">
          <router-view></router-view>
        </el-col>
      </el-row>
    </div>
  </div>


</template>

<script>
import router from '@/router'
import Parallax from 'vue-parallaxy'

export default {
  name: 'app',
  methods: {
    goHome () {
      router.push('/')
    }
  },
   components: {
      Parallax
    }
}



</script>


<style lang="sass">
@import "./assets/theme";

body
  background-image : url("https://www.pixelstalk.net/wp-content/uploads/2016/05/Bing-background-Images-1.jpg")
  background-size: contain
  /*background-repeat: no-repeat*/

</style>




