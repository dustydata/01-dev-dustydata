<script>
	import Circle from '$lib/Circle.svelte'
	import Rect from '$lib/Rect.svelte'
    import DustyDataSVG from '$lib/DustyDataSVG.svelte'
	
	let selected = DustyDataSVG 
</script>


<!-- <h1>DustyData</h1> -->
<svelte:component this={selected} />
<button on:click={()=> selected = DustyDataSVG}>
	Make it DustyData
</button>

<button on:click={()=> selected = Rect}>
	Make it square
</button>

<button on:click={()=> selected = Circle}>
	Make it circle
</button>

<style>
	:global(svg) {
		max-width: 400px;
		display: block
	}
</style>