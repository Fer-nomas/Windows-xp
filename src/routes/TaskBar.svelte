<script>
	let time;
	function darLaHora() {
		let fecha = new Date();
		let hh = fecha.getHours();
		let mm = fecha.getMinutes();

		hh = hh < 10 ? '0' + hh : hh;
		mm = mm < 10 ? '0' + mm : mm;

		time = hh + ':' + mm;
		return time;
	}
	setInterval(() => {
		darLaHora();
	}, 100);
</script>

<div class="container">
	<div class="inicio">
		<img
			src="https://cdn.discordapp.com/attachments/749326094800519179/1100616253296615464/si_clipdrop-background-removal.png"
			alt="si"
			srcset=""
		/>
	</div>
	<div class="hora">
		<img
			src="https://cdn.discordapp.com/attachments/749326094800519179/1104945951954714634/Freestyle-Test-1-2023-02-11-10-54-08-640x480-removebg-preview_1.png"
			alt=""
			srcset=""
		/>
		<div class="fecha">{time}</div>
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
		height: 3.5em;
		width: 100%;
		background-color: #235bd8;
		position: absolute;
		box-shadow: 0px 5px 5px inset #3680e5;
		bottom: 0;
	}
	.inicio {
		cursor: pointer;
		display: flex;
		top: 0;
		left: 0;
		height: 3.5em;
		position: absolute;
	}
	.inicio img {
		height: 3.5em;
	}
	.hora {
		cursor: pointer;
		display: flex;
		position: absolute;
		align-items: center;
		height: 3.5em;
		width: 10.5em;
		right: 0;
		top: 0;
		background-color: #108be7;
		border-radius: 10px 0px 0px 10px;
		box-shadow: solid 0px 10px 10px #178ac9;
		box-shadow: inset 0em 0.4em 10px #7ebee0;
	}
	.hora img {
		height: 3.5em;
		position: relative;
		display: flex;
		left: 0;
		align-self: flex-start;
	}
	.fecha {
		font-family: 'Open Sans';
		color: #dee;
		position: absolute;
		right: 0;
		padding: 20px;
		font-size: 1.26em;
		font-weight: 900;
	}
</style>
