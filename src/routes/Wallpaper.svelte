<script>
	import Apps from './Wallpaper-Apps.svelte';
</script>

<div class="container">
	<Apps />
</div>

<style>
	div {
		display: inline;
		border: 2px solid black;
		padding: 20px;
	}
	.container {
		display: flex;
		flex-wrap: wrap;
		height: calc(100vh - 6.7em);
	}
</style>
