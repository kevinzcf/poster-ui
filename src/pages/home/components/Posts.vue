<template>
  <div class="posts">
	<div class="post" v-for="item of posts" :key="item.id">
		<div class="title">{{item.title}}</div>
		<div class="body">{{item.body}}</div>
	</div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
	name: 'posts',
	data () {
		return {
			posts:[]
		}
	},
	mounted(){
		this.getPosts();
	},
	methods:{
		getPosts(){
			var url = "http://jsonplaceholder.typicode.com/posts?userId=1";
			axios.get(url).then((response)=>{
				this.posts=response.data;
			});
			this.posts = "loading...."
		}
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