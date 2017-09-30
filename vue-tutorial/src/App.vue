<template>
  <div id="wrapper">
    <!--导航条-->
    <nav class="navbar navbar-inverse">
      <div class="container-fluid">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
          <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
            <span class="sr-only">Toggle navigation</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <a class="navbar-brand" href="#"><i class="glyphicon glyphicon-time"></i>计划板</a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
          <ul class="nav navbar-nav">
            <li><router-link to="/home">首页</router-link></li>
            <li><router-link to="/time-entries">计划列表</router-link></li>
          </ul>
        </div><!-- /.navbar-collapse -->
      </div><!-- /.container-fluid -->
    </nav>
    <div class="container-fluied">
      <div class="container">
        <div class="col-sm-3">
          <sidebar></sidebar>
        </div>
        <div class="col-sm-9">
          <router-view></router-view>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Home from './components/Home.vue';
import TimeEntries from './components/TimeEntries.vue';
import Sidebar from './components/Sidebar.vue'


export default {
  name: 'app',
  components: {
    'Home':Home,
    'sidebar': Sidebar,
    'time-entries':TimeEntries
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.navbar-inverse .navbar-brand{
  color: #fff;
}
.navbar-inverse .navbar-nav > li > a{
  color: #fff;
}
  .navbar{
    /*margin-bottom: 0;*/
  }
  .main{
    width: 100%;
  }
</style>
