<script>
	import TaskBar from './TaskBar.svelte';
	import Wallpaper from './Wallpaper.svelte';
	import Web from './Web.svelte';
	import { store } from '../store.js';
	import { onDestroy } from 'svelte';

	let valueVar;

	const unsubscribe = store.subscribe((value) => {
		valueVar = value;
	});
	onDestroy(unsubscribe);
	$: console.log(valueVar);
</script>

{#if valueVar == 0}
	<Wallpaper />
{:else if valueVar == undefined}
	<Web />
{/if}

<TaskBar />

<style>
	:global(body) {
		background-image: url('https://fondosmil.com/fondo/9723.jpg');
		background-repeat: no-repeat;
		background-size: cover;
		background-attachment: fixed;
		background-position: center;
		margin: 0;
		padding: 0;
		overflow: hidden;
	}
</style>
