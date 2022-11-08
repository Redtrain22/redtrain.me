<script lang="ts">
	export let name: string;
	export let link: string;
</script>

<a href={link}>
	<button>{name}</button>
</a>

<style>
	button {
		border-radius: 100px;
		padding: 5px;
		padding-left: 10px;
		padding-right: 10px;
		text-align: center;
		background-color: transparent;
		border-color: white;
		color: white;
		font-size: 15pt;
		font-family: "Source Code Pro", monospace;
	}
</style>
