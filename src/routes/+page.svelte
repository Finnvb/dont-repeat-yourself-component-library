<script>
	import Clock from 'ilojo-bar-components/components/Clock.svelte';
	import StoryPlateBtn from 'ilojo-bar-components/components/StoryPlateBtn.svelte';
	import SmallFooter from 'ilojo-bar-components/components/SmallFooter.svelte';
	import '../styles/global.css';

	// import Form from 'ilojo-bar-components/components/FormComponents/Form.svelte';
</script>

<svelte:head>
	<title>Ilojo Bar - component Library</title>
</svelte:head>

<main>
	<h1>Stories of the <br /> ILOJO BAR</h1>

	<h2>Discover the stories of the <br /> demolished bar in Lagos</h2>

	<section>
		<div>
		<StoryPlateBtn
			storyPlateImage={'goldplate.png'}
			storyLink={'overview'}
			storyLinkText={'Discover Stories'}
			color={'#593a08'}
			height={'7rem'}
		/>

		<StoryPlateBtn
		storyPlateImage={'goldplate2.png'}
		storyLink={'form'}
		storyLinkText={'Create Story'}
		color={'#101010'}
		height={'5rem'}
	/>
	</div>

		<img src="cdf-1950s.png" alt="Ilojo-bar" />

		<Clock />
</section>
<!-- <Form/> -->
	<SmallFooter companyName={'Finn van Bekkum'} />
</main>

<style>
	main {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		/* height: 100vh; */
	}

	h1,
	h2 {
		text-align: center;
	}

	h1 {
		font-size: 4rem;
	}

	h2 {
		font-size: 1.5rem;
		margin: 2rem 0;
	}

	section img {
		width: 450px;
		height: 100%;
		box-shadow: 0px 0px 20px 1px #000;
		border: 7px solid var(--red);
		margin-top: 1rem;
	}

	section {
		display: flex;
		justify-content: space-around;
		align-items: center;
		width: 100%;
		margin: 2rem 0;
	}

	div{
		display: flex;
		flex-direction: column;
	}

	@media (max-width: 40em) {
		section {
			flex-direction: column-reverse;
		}

		h1 {
			font-size: 3rem;
		}

		h2 {
			font-size: 1.2rem;
		}

		section img {
			margin-bottom: 2rem;
			width: 300px;
		}

		.clock {
			width: 30px;
		}
	}
</style>
