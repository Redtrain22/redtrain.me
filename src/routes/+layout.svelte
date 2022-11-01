<script lang="ts">
	import NavBox from "$lib/NavBox.svelte";
	import { page } from "$app/stores";
	import Oneko from "$lib/Oneko.svelte";

	const navBarData = [
		{ imgSrc: "/favicon.png", location: "/", name: "Logo" },
		{ imgSrc: undefined, location: "/about", name: "About" },
		{ imgSrc: undefined, location: "/contact", name: "Contact" }
	];

	let enableOneko = true;
</script>

<nav>
	{#each navBarData as navData}
		<li class:selected={$page.url.pathname.length == navData.location.length && $page.url.pathname.includes(navData.location)}>
			<NavBox {...navData} />
		</li>
	{/each}
</nav>

{#if enableOneko}
	<Oneko />
{/if}

<slot />

<footer>
	<p>&copy; Redtrain22 2022</p>
	<button on:click={() => (enableOneko = !enableOneko)}> {enableOneko ? "Hide" : "Show"} Cat </button>
</footer>

<style>
	nav {
		background-color: #b3a8a8;
		text-align: center;
		font-size: 150%;
	}

	nav > li {
		display: inline-block;
		vertical-align: middle;
		padding-left: 4px;
		padding-right: 4px;
	}

	nav > .selected {
		background-color: black;
		padding-left: 8px;
		padding-right: 8px;
		border-radius: 15px;
	}

	footer {
		align-items: center;
		display: flex;
		position: fixed;
		left: 0;
		bottom: 0;
		width: 100%;
		background-color: black;
	}

	footer > p {
		padding-right: 10px;
		padding-left: 10px;
	}

	footer > button {
		border: none;
		text-decoration: none;
		display: inline-block;
		background-color: #f44336;
		color: white;
		text-align: center;
		font-size: large;
		padding: 8px;
	}
</style>
