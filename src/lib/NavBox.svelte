<script lang="ts">
	export let imgSrc: string | undefined = undefined;
	export let name: string;
	export let location: string;
</script>

{#if imgSrc != undefined}
	<a href={location}> <img src={imgSrc} alt={name} /> </a>
{:else}
	<a href={location}>{name}</a>
{/if}

<style>
	img {
		width: 64px;
		height: 64px;
	}

	a:any-link,
	a:visited {
		text-decoration: none;
		color: green;
	}
</style>
