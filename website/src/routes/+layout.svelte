<script>
	import Header from './Header.svelte';
	import './styles.css';
	import github from '$lib/images/github.svg';
	import instagram from '$lib/images/instagram.svg';
	import linkedin from '$lib/images/linkedin.svg';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<div>
		<a href="https://github.com/maximilian-graf2019">
			<img src={github} alt="GitHub" />
		</a>
		<a href="https://www.instagram.com/grafmaximilian/">
			<img src={instagram} alt="Instagram" />
		</a>
		<a href="https://www.linkedin.com/in/maximilian-graf-8a8583197/">
			<img src={linkedin} alt="LinkedIn" />
		</a>
		</div>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	footer img {
		width: 50px;
		height: 50px;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
