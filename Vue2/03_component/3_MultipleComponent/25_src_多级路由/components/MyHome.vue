<template>
  <div>
    <h2>Home组件内容</h2>
    <div>
      <ul className="nav nav-tabs">
        <li>
          <router-link className="list-group-item" active-class="active" to="/home/news">News</router-link>
        </li>
        <li>
          <router-link className="list-group-item" active-class="active" to="/home/message">Message</router-link>
        </li>
      </ul>
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
export default {
  name: "MyHome"
}
</script>

<style scoped>

</style>