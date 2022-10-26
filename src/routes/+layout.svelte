<script lang="ts">
	import Heading from '../lib/Heading.svelte';
	import Links from '../lib/Links.svelte';
</script>

<main>
	<div id="header" />
	<div class="left" />
	<div class="stuff">
		<Heading />
		<hr />
		<br /><br />
		<Links />
		<br /><br />
		<nav>
			<button
				class="button"
				on:click={() => {
					// window.location.href = base + '/';
				}}
			>
				<a class="new-a" href="/">Home</a>
			</button>
			<button
				class="button2"
				on:click={() => {
					// window.location.href = base + '/Info';
				}}
			>
				<a class="new-a" href="/Info">Info about me</a></button
			>
			<button
				class="button"
				on:click={() => {
					// window.location.href = base + '/Coins';
				}}><a class="new-a" href="/Coins">Coins</a></button
			>
		</nav>
		<slot />
	</div>
	<div class="right" />
	<div id="footer" />
</main>

<style>
	* {
		max-width: 1000px;
		margin: auto;
	}

	.new-a {
		color: white;
	}
	.button {
		background-color: rgb(202, 201, 103);
		border: none;
		color: white;
		padding: 15px 32px;
		text-align: center;
		text-decoration: none;
		display: inline-block;
		font-size: 16px;
	}
	.button2 {
		background-color: rgb(50, 6, 59);
		border: none;
		color: white;
		padding: 15px 32px;
		text-align: center;
		text-decoration: none;
		display: inline-block;
		font-size: 16px;
	}

	div {
		border-radius: 5px;
		position: relative;
	}

	#header {
		height: 40px;
		width: 100%;
		background-color: rgb(50, 6, 59);
		z-index: 1;
	}

	#footer {
		height: 50px;
		width: 100%;
		background-color: rgb(50, 6, 59);
		clear: both;
		position: relative;
	}

	.left {
		height: 1500px;
		width: 45px;
		background-color: rgb(202, 201, 103);
		float: left;
		position: inherit;
	}

	.right {
		height: 1500px;
		width: 45px;
		background-color: rgb(202, 201, 103);
		float: right;
		position: inherit;
	}

	.stuff {
		display: inline-block;
		margin-top: 6px;
		margin-left: 55px;
		width: 75%;
		height: 1500px;
	}

	@media only screen and (max-width: 430px) {
		.left,
		.right {
			display: none;
		}
		.stuff {
			width: 100%;
			margin-left: 10px;
		}
	}
</style>
