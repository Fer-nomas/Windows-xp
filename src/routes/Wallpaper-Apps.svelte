<script>
	import { draggable } from '@neodrag/svelte';
	import { store } from '../store.js';

	let appbag = 'appbag';
</script>

<div class="container">
	<div
		use:draggable={{ bounds: 'body', grid: [50, 50] }}
		class={appbag}
		on:neodrag:end={(e) => (appbag = 'appbag')}
		on:neodrag:start={(e) => (appbag = 'appbagmove')}
	>
		<!-- svelte-ignore a11y-click-events-have-key-events -->
		<img
			id="1"
			src="https://cdn.discordapp.com/attachments/749326094800519179/1100628038703644692/sshot-24_clipdrop-background-removal_clipdrop-enhance.png"
			alt=""
			srcset=""
		/>
		<span>About Us</span>
	</div>
	<div
		use:draggable={{ bounds: 'body', grid: [50, 50] }}
		class={appbag}
		on:neodrag:end={(e) => (appbag = 'appbag')}
		on:neodrag:start={(e) => (appbag = 'appbagmove')}
	>
		<img
			id="2"
			src="https://cdn.discordapp.com/attachments/749326094800519179/1100629481506488352/sshot-425_clipdrop-background-removal_clipdrop-enhance.png"
			alt=""
			srcset=""
		/>
		<span>Contact</span>
	</div>
	<div
		use:draggable={{ bounds: 'body', grid: [50, 50] }}
		class={appbag}
		on:neodrag:end={(e) => (appbag = 'appbag')}
		on:neodrag:start={(e) => (appbag = 'appbagmove')}
	>
		<img
			id="3"
			src="https://cdn.discordapp.com/attachments/749326094800519179/1100623886313328680/sshot-42-removebg-preview_1.png"
			alt=""
			srcset=""
		/>
		<span>Jobs</span>
	</div>
</div>

<style>
	* {
		user-select: none;
	}
	*::selection {
		background: none;
	}
	*::-moz-selection {
		background: none;
	}
	.container {
		max-height: 200px;
		max-width: 200px;
		display: flex;
		justify-content: start;
		align-items: start;
		flex-direction: column;
		gap: 20px;
	}
	.appbag {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		cursor: pointer;
	}

	.appbag img {
		width: 5em;
		display: flex;
		justify-self: end;
		align-self: end;
	}
	.appbag span {
		font-family: 'Open Sans';
		font-size: 15px;
		font-weight: 900;
	}
	.appbagmove {
		cursor: grab;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	.appbagmove img {
		width: 5em;
		display: flex;
		justify-self: end;
		align-self: end;
	}
	.appbagmove span {
		font-family: 'Open Sans';
		font-size: 15px;
		font-weight: 900;
	}
</style>
