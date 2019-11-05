<template>
  <div class="user">
	<div class="user-left">
		<div>{{user.name}}</div>
		<div>{{user.email}}</div>
		<div>{{user.phone}}</div>
		<div>{{user.website}}</div>
	</div>
	<div class="user-right">
		<div>{{user.address.street}}</div>
		<div>{{user.address.suite}}</div>
		<div>{{user.address.city}}</div>
		<div>{{user.address.zipcode}}</div>
	</div>
  </div>
</template>

<script>
export default {
	name: "user",
	props: {
		user: {}
	}
}
</script>

<style lang="stylus" scoped>
	.user
		display: flex
		height: 6rem
		text-align: center
		.user-left
			flex: 1
			float: left
		.user-right
			flex: 1
			float: right
</style>