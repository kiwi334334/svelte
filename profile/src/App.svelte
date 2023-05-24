<script>
	import Menubar from "./components/menubar.svelte";
	let name = "";
	let issignedin = false
	function signin() {
		if (name === "ENW") {
			issignedin = true
		}
		else{
			issignedin = false
		}
	}
</script>

<Menubar />
<main>
	<input class="signin" id="sign" bind:value={name} placeholder="type name here"/>
	<button class="signin" id="sign2" on:click={signin}>Submit Name</button>
	<div id="" class="hid">
		{#if (issignedin)}
			<div>
				<h1>hello Elias How Are You Today.</h1>
			</div>
		{/if}
	</div>
</main>

<style>
	.signin {
		margin-left: auto;
	}
	main {
		background-color: snow;
		width: 100vw;
		height: 100vh;
	}
</style>
