<script>
	import { slide } from "svelte/transition";
	import { quintOut } from 'svelte/easing';
	export let text;
	export let skills;
	let hoverBool = false;

	function reveal() {
		hoverBool=true;
	}
	function hide() {
		hoverBool=false;
	}
</script>
<!-- svelte-ignore a11y-no-static-element-interactions -->
<div class="main" on:mouseenter={reveal} on:mouseleave={hide}>
	<p>- {text}</p>
	{#if hoverBool}
			<ul transition:slide={{delay: 250, duration: 500, easing: quintOut, axis: 'y' }}>
				{#each skills as s}
					<li>{s}</li>
				{/each}
			</ul>
	{/if}
</div>
<style>
	ul {
		padding: 0.25em 1em;
		background-image: linear-gradient(to right, rgb(200,200,200), rgb(125,125,125), transparent);
		list-style-position: inside;
		color: black;
		opacity: 0.75;
	}
</style>