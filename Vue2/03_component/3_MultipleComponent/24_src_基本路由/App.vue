<template>
  <div>
    <div class="row">
      <div class="col-xs-offset-2 col-xs-8">
        <div class="page-header"><h2>Vue Router Demo</h2></div>
      </div>
    </div>
    <div class="row">
      <div class="col-xs-2 col-xs-offset-2">
        <div class="list-group">
          <router-link class="list-group-item" active-class="active" to="/about">MyAbout</router-link>
          <router-link class="list-group-item" active-class="active" to="/home">MyHome</router-link>
          <!--<a class="list-group-item active" href="./about.html">About</a>-->
          <!--<a class="list-group-item" href="./home.html">Home</a>-->
        </div>
      </div>
      <div class="col-xs-6">
        <div class="panel">
          <div class="panel-body">
            <!--指定组件的呈现位置-->
            <router-view></router-view>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "App",
  }
</script>

