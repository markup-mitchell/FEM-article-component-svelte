<script>
	import Card from './components/Card.svelte';
	let data = {
		featured_image: './images/drawers.jpg',
		featured_image_alt: "Framed pictures and a vase of wild grass on top of a chest of drawers against a whitewashed brick wall.",
		author_image: './images/avatar-michelle.jpg',
		author_name: "Michelle Appleton",
		publish_date: "28 Jun 2020",
		content_heading: "Shift the overall look and feel by adding these wonderful touches to furniture in your home",
		content_text: "Ever been in a room and felt like something was missing? Perhaps it felt slightly bare and uninviting. I’ve got some simple tips to help you make any room feel complete."
	}
	
</script>

<main>
	<Card {data} />
</main>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Manrope:wght@200&display=swap');
	main {
		min-height: 100vh;
		background-color:#ECF2F8;
		display: flex;
		justify-content: center;
		align-items: center;
		padding: 0 1.5rem;
		font-family: 'Manrope', sans-serif;
	}


</style>

