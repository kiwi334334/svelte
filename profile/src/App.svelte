<script>
	import Menubar from "./components/menubar.svelte";
	let name = "";
	let feeling = 1;
	let issignedin = false;
	function signin() {
		if (name === "ENW") {
			issignedin = true;
		} else {
			issignedin = false;
		}
	}
</script>

<Menubar />
<main>
	<input
		class="signin"
		id="sign"
		bind:value={name}
		placeholder="type name here"
	/>
	<button class="signin" id="sign2" on:click={signin}>Submit Name</button>
	<div id="" class="hid">
		{#if issignedin}
			<div>
				<h1>hello Elias How Are You Today.</h1>
			</div>
		{:else}
			<center>
				<h1>
					Welcome To My Website<br/><small>How are you feelling today</small>
				</h1>
				<select bind:value={feeling}>
					<option value="select">-select-</option>
					<option value="good">Good</option>
					<option value="okay">Okay</option>
					<option value="bad">Bad</option>
					<option value="horrible">Horrible</option>
				</select>
				{#if (feeling === "select")}
					<p>p</p>
				{:else if (feeling === "good")}
					<div>
						<h1>Thats good!</h1>
					</div>
				{:else if (feeling === "okay")}
					<div>
						<h1>welp '_'</h1>
					</div>
				{:else if (feeling === "bad")}
					<div>
						<h1>Hope You feel better</h1>
					</div>
				{:else if (feeling === "horrible")}
					<div>
						<h1>Ha! Sucks for you!</h1>
					</div>
				{/if}
			</center>
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
