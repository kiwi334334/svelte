<script>
	import Menubar from "./components/menubar.svelte";
	let name = "";
	function signin() {
		if (name === "ENW") {
			start();
		}
	}
	function start() {
		document.getElementById("sign").style.display = "none";
		document.getElementById("sign2").style.display = "none";
	}
</script>
<Menubar />
<main>
	<input class="signin" id="sign" bind:value={name} placeholder="type name here" />
	<button class="signin" id="sign2" on:click={signin}>Submit Name</button>
</main>

<style>
	.signin{
		margin-left: auto;
	}
	main {
		margin-left: auto;
		background-color: snow;
		width: 100vw;
		height: 100vh;
	}
</style>
