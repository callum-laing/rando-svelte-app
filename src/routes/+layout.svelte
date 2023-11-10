<script>
	import '../lib/styles/global.css';
	import Header from '../lib/components/Header.svelte';
	import Footer from '../lib/components/Footer.svelte';
</script>

<div class="layout">
	<Header />
	<main>
		<div class="grid-wrapper">
			<span>1</span>
			<span>1</span>
			<span>1</span>
			<span>1</span>
		</div>
	</main>
	<slot />
	<Footer />
</div>

<style>
	.layout {
		height: 100%;
		display: grid;
		grid-template-rows: auto 1fr auto;
		margin-inline: auto;
	}

	.grid-wrapper {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		grid-template-rows: repeat(2, 1fr);
		height: 100%;
		gap: 5px;
	}

	.grid-wrapper > span {
		height: 100%;
		background-color: grey;
	}

	h1 {
		text-align: center;
	}
</style>
