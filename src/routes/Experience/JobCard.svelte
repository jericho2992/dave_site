<script>
	import Bullets from "./Bullets.svelte";
	export let title;
	export let bullets;
	export let employer;
	function openSkill(event) {
		console.log(event.target)
	}
</script>
<div class="main">
	<div class="title-div"><h3>{title}</h3><h5>{employer}</h5></div>
	<div class="bullets-div">
		{#each bullets as b}
			<Bullets bind:text={b.text} bind:skills={b.skills}></Bullets>
		{/each}
	</div>
</div>
<style>
	.main {
		border-top: solid white 3px;
		padding: 0.1em 1.5em 1em 1.5em;
		margin: 2em 2em 0em 2em;
		min-width: 55vw;
		opacity: 0.8;
		background: linear-gradient(rgb(0,50,50), rgb(0,75,75), transparent)
	}
	.main:hover {
		opacity: 1;
		background: rgb(0,60,60);
	}
	h3 {
		margin-bottom: 0;
		text-decoration: underline;
	}
	h5 {
		margin-top: 0.4em;
	}
</style>