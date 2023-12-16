<script>
	import Background from "./components/background/Background.svelte";
	import Heading from "./components/Heading.svelte";
	import {fade} from "svelte/transition";
	import Projects from "./components/Projects.svelte";
	import About from "./components/About.svelte";


	let pageIndex = 0;

	function changePageIndex(newIndex){
		pageIndex = newIndex;
	}
	function returnButtonPress(){
		pageIndex = 0;
	}

</script>


<main>

	{#if pageIndex === 0}
		<Heading tranistion:fade {changePageIndex}/>
		{:else if pageIndex === 1}
			<Projects tranistion:fade {returnButtonPress}/>
		{:else if pageIndex === 2}
			<About tranistion:fade {returnButtonPress}/>
	{/if}

<!--	<Projects />-->

</main>
<Background />

<style>
	main {
		text-align: center;
		/*padding: 1em;*/
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>