<template>
  <div class="posts">
	<div class="post" v-for="item of posts" :key="item.id">
		<div class="title">{{item.title}}</div>
		<div class="body">{{item.body}}</div>
	</div>
  </div>
</template>

<script>
export default {
	name: 'posts',
	props: {
		posts: []
	}
}
</script>

<style lang="stylus" scoped>
	.post
		text-align: center
		padding: 2rem
		.title	
			color: #999
			font-style: italic
			font-size: 20px
		.body
			margin-top: 0.5rem
</style>