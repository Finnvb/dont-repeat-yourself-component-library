<script>
	import Header from 'ilojo-bar-components/components/Header.svelte';
	import Link from 'ilojo-bar-components/components/Link.svelte';
	import Form from 'ilojo-bar-components/components/FormComponents/Form.svelte';
    import SmallFooter from 'ilojo-bar-components/components/SmallFooter.svelte';
	import * as prismicH from '@prismicio/helpers';
	export let data;
</script>


<Header>
	{#each data.document as data}
		<Link link={data.uid} linkTitle={data.uid} />
	{/each}
</Header>
<main>
    <div>
	<Form />
</div>
<SmallFooter companyName={'Finn van Bekkum'}/>
</main>

<style>
	main {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		/* height: 100vh; */
	}

    div{
        margin-top: 4rem;
    }
</style>
