<template>
  <ul>
    <li :style="{opacity}">se ya na (|-|)</li>
    <li>news001 <input type="text"> </li>
    <li>news002 <input type="text"> </li>
    <li>news003 <input type="text"> </li>
  </ul>
</template>

<script>
  export default {
    name: "MyNews",
    data(){
      return {
        opacity:1
      }
    },
    // commit
    activated() {
      console.log('News组件被激活了')
      this.timer = setInterval(() => {
        console.log('@')
        this.opacity -= 0.01
        if(this.opacity <= 0) this.opacity = 1
      },16)
    },
    deactivated() {
      console.log('News组件失活了')
      clearInterval(this.timer)
    },
  }
</script>

<style scoped>

</style>