<script>
	import WindowSection from 'ilojo-bar-components/components/WindowSection.svelte';
	import Window from 'ilojo-bar-components/components/Window.svelte';
	import StoryPlateBtn from 'ilojo-bar-components/components/StoryPlateBtn.svelte';
	import Header from 'ilojo-bar-components/components/Header.svelte';
	import ScrollToTopButton from 'ilojo-bar-components/components/ScrollToTopButton.svelte';

	import * as prismicH from '@prismicio/helpers';
	export let data;

	const { document } = data;

	console.log(document);
</script>

<Header />

<main>
	<section>
		<WindowSection />

		{#each data.document as data}
			<Window
				storyImage={data.data.storyimages[0].image1.url}
				storyTitle={data.data.storytitle[0].text}
				altTag={data.data.storytitle[0].text}
			/>

			<StoryPlateBtn
				storyPlateImage={'goldplate3.png'}
				storyLink={data.uid}
				storyLinkText={'Discover Story'}
				color={'#000000'}
				height={'6rem'}
			/>
		{/each}

		<WindowSection />
	</section>

	<ScrollToTopButton buttonLink={'overview'} />
</main>

<style>
	main {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: row;
		flex-wrap: wrap;
		margin: 4rem 2rem;
		gap: 4rem;
		position: relative;
	}
</style>
