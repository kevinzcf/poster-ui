<template>
  <div class="home">
	<user></user>
	<posts></posts>
  </div>
</template>

<script>
import User from './components/User'
import Posts from './components/Posts'
export default {
	name: 'Home',
	components: {
		User,
		Posts
	}
}
</script>