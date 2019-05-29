<template>
	<el-card
		shadow="hover"
		:body-style="{padding: 0}"
		class="post"
	>
		<header slot="header" class="post-header">
			<h3>Post tittle</h3>
			<small>
				<i class="el-icon-time"></i>
				{{ new Date().toLocaleString() }}
			</small>
		</header>
		<div class="post-body">
			<img 
				src="https://stilist.ru/uploads/salon/6435/9193ec9ba3c92d810152c1cbef4259e3/10424985_359472567559454_684477581380200076_n_0.jpg" 
				alt="post image" 
				class="post-img"
			>
		</div>
		<footer class="post-footer">
			<el-button round @click="openPost">Открыть</el-button>
			<span>
				<i class="el-icon-message">12</i>
			</span>
		</footer>
	</el-card>
</template>

<script>
export default {
	methods: {
		openPost () {
			const id = 'test-id'
			this.$router.push(`/post/${id}`)
		}
	}
}
</script>

<style lang="scss" scoped>

	.post {
		margin-bottom: 1.5rem;
	}

	.post-header {
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.post-img {
		width: 100%;
		height: auto;
	}

	.post-footer {
		padding: 1rem;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

</style>


