<script>
	// import Header from '../../lib/components/Header.svelte';
	// import Footer from '../../lib/components/Footer.svelte';
	// import Button from '$lib/components/Button.svelte';
	// import ScrollToTopButton from '../../lib/components/ScrollToTopButton.svelte';
	import * as prismicH from '@prismicio/helpers';
	export let data;

	const { document } = data;

	console.log(document);





</script>

<!-- <Header /> -->

<main>
	{#each data.document as data}
		<section>
			<div class="image-container">
				<img class="storyimage" src={data.data.storyimages[0].image1.url} alt="test" />
			</div>

			<div class="window">
				<img class="window" src="window.svg" alt="window" />
				<img class="windowLeft" src="windowLeft.svg" alt="window" />
				<img class="windowRight" src="windowRight.svg" alt="window" />
				<div class="test" />
			</div>

			<h2>{@html prismicH.asHTML(data.data.storytitle)}</h2>

			<!-- <Button source={"goldplate.png"} link={data.uid} linktext={'Discover'} height={'4rem'} color={("#6c5334")} /> -->
		</section>
	{/each}

	<!-- <ScrollToTopButton uid="overview" /> -->
	
</main>