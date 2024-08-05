<script>
	let { title, ancher } = $props();
</script>

<button class="p-[1px] inline-block rounded-b-lg rounded-tl-lg rounded-tr-3xl bg-btn">
	<div
		class="rounded-b-lg rounded-tl-lg rounded-tr-3xl transform transition-all ease-in-out delay-150 hover:text-purple-600 bg-[#131216] flex items-center justify-center px-4 py-2 text-white uppercase"
	>
		<a href={ancher ? ancher : '#'}>
			{title}
		</a>
	</div>
</button>
