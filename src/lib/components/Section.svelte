<script>
	let { renderedSection } = $props();
</script>

{#snippet PlusSvg(classes)}
	<svg class={classes} width="11" height="11" fill="none">
		<path
			d="M7 1a1 1 0 0 0-1-1H5a1 1 0 0 0-1 1v2a1 1 0 0 1-1 1H1a1 1 0 0 0-1 1v1a1 1 0 0 0 1 1h2a1 1 0 0 1 1 1v2a1 1 0 0 0 1 1h1a1 1 0 0 0 1-1V8a1 1 0 0 1 1-1h2a1 1 0 0 0 1-1V5a1 1 0 0 0-1-1H8a1 1 0 0 1-1-1V1z"
			fill="#ada8c4"
		/>
	</svg>
{/snippet}
{#snippet Pluses()}
	{@render PlusSvg('absolute -top-[0.4rem] -left-[0.4rem]')}
	{@render PlusSvg('absolute -bottom-[0.4rem] -left-[0.4rem]')}
	{@render PlusSvg('absolute -top-[0.4rem] -right-[0.4rem]')}
	{@render PlusSvg('absolute -bottom-[0.4rem] -right-[0.4rem]')}
{/snippet}
<div
	class="relative flex justify-center items-center mt-[100px] text-white w-full border border-gray-700 m-10"
>
	{@render Pluses()}
	<svelte:component this={renderedSection} />
</div>
