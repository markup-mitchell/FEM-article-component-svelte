<script>
	import Card from './components/Card.svelte';
	import Content from './components/Content.svelte';
	let ArticleImage = '../images/drawers.jpg';
</script>

<main>
	<Card>
		<img slot="article__image" src={ArticleImage} alt="">
		<div slot="article__content">
			<Content />
		</div>
	</Card>
</main>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Manrope:wght@200&display=swap');
	main {
		min-height: 100vh;
		background-color:#ECF2F8;
		display: flex;
		justify-content: center;
		align-items: center;
		padding: 0 1.5rem
	}

	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: 0;
	}
</style>

