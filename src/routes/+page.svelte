<script lang="ts">
	import Socials from "$lib/Socials.svelte";

	const socials = [
		{ name: "Discord", link: "https://discord.com/users/206353028318494720" },
		{ name: "Steam", link: "https://steamcommunity.com/id/redtrain22/" },
		{ name: "MyAnimeList", link: "https://myanimelist.net/profile/Redtrain22" },
		{ name: "GitHub", link: "https://github.com/Redtrain22" }
	];
</script>

<div>
	<h1>I'm Red!</h1>
	<p>You can find out more about me, or find some resources that I make public</p>
	<p>If you're curious about what I do in my free time or want to reach out to me you can find me using one of the links below</p>

	<table>
		{#each socials as social}
			<tr>
				<td><Socials {...social} /></td>
			</tr>
		{/each}
	</table>
</div>

<style>
	h1 {
		font-size: 30pt;
	}

	p {
		font-size: 14pt;
	}

	div {
		text-align: center;
		padding: 100px;
		display: grid;
	}

	table {
		/* padding: 0px 0px 10px 10px; */
		margin-left: auto;
		margin-right: auto;
		display: flex;
		align-items: center;
		border-color: black;
	}
	tr {
		align-items: center;
		padding-left: 5px;
		padding-right: 5px;
	}
</style>
