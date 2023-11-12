<script>
	import ProjTwo from './ProjTwo.svelte';
	let yes = false;
	let start = false;
</script>

<div class="form">
	<h2>I want to play a game...</h2>
	<label>Are you ready?<input type="checkbox" bind:checked={yes} /></label>

	{#if yes}
		<p>Good choice.</p>
	{:else}
		<p>There are 3 games, beat each one to progress.</p>
	{/if}

	<button disabled={!yes} type="button" on:click={() => (start = true)}>Start</button>

	{#if start && yes}
		<ProjTwo />
	{/if}
</div>

<style>
	.form {
		display: flex;
		flex-direction: column;
		align-items: center;
		background-color: grey;
	}

	button {
		width: 20%;
		border-radius: 5px;
		/* box-shadow: 2px 2px; */
	}

	button:not([disabled]):hover {
		box-shadow: 2px 2px;
		font-weight: bold;
		color: black;
	}
</style>
