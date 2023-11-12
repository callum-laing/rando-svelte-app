<div>
	<img src="bull.svg" alt="" />
	<h1>Playground</h1>
	<h2>CDL</h2>
</div>

<style>
	div {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		grid-template-rows: 1;
		text-align: center;
		border-bottom: 1px solid black;
		width: 100%;
	}

	div > p {
		padding: 0;
		height: 100%;
		padding-bottom: 10px;
	}

	h2 {
		text-align: center;
		letter-spacing: 5px;
	}

	img {
		height: 50px;
		padding: 10px;
		transition: transform 0.7s ease-in-out;
	}

	img:hover {
		transform: rotate(360deg);
	}
</style>
