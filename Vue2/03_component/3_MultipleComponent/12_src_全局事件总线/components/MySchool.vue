<template>
	<div class="school">
		<h2>学校名称：{{name}}</h2>
		<h2>学校地址：{{address}}</h2>
	</div>
</template>

<script>
	export default {
		name:'MySchool',
		data() {
			return {
				name:'尚硅谷',
				address:'北京',
			}
		},
    mounted() {
      console.log('school',this.x)
      this.$bus.$on('hello',(data)=>{
        console.log('This is School and received data:',data)
      })
    },
    // 销毁之前解绑组件，避免占用事件hello
    beforeDestroy() {
      this.$bus.off('hello')
    }
  }
</script>

<style scoped>
	.school{
		background-color: skyblue;
		padding: 5px;
	}
</style>