<template>
  <div class="home">
	<user :user="user"></user>
	<posts :posts="posts"></posts>
  </div>
</template>

<script>
import axios from 'axios'
import User from './components/User'
import Posts from './components/Posts'
export default {
	name: 'Home',
	components: {
		User,
		Posts
	},
	data () {
		return {
			user:{},
			posts:[]
		}
	},
	mounted(){
		this.getUser();
		this.getPosts();
	},
	methods:{
		getUser(){
			var url = "http://jsonplaceholder.typicode.com/users/1";
			axios.get(url).then((response)=>{
				this.user=response.data;
			});
			this.user = "loading....";
		},
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