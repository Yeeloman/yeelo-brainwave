<script>
	let { title, ancher } = $props();

	let isOpen = $state(false);

	const toggleOpen = () => {
		isOpen = !isOpen;
	};
</script>

<button
	class="p-[1px] relative inline-block rounded-b-lg rounded-tl-lg rounded-tr-3xl bg-btn"
	onclick={toggleOpen}
>
	<div
		class="rounded-b-lg rounded-tl-lg rounded-tr-3xl transform transition-all ease-in-out delay-150 hover:text-purple-600 bg-[#131216] flex items-center justify-center px-4 py-2 text-white uppercase"
	>
		<a href={ancher ? ancher : '#test'} class="md:hidden">
			{title}
		</a>
		<div class="size-7 hidden md:block"></div>
		<div
			class="hidden md:block absolute h-1 w-8 rounded bg-white transition-all duration-500 before:absolute before:h-1 before:w-8 before:-translate-x-4 before:-translate-y-3 before:rounded before:bg-white before:transition-all before:duration-500 before:content-[''] after:absolute after:h-1 after:w-8 after:-translate-x-4 after:translate-y-3 after:rounded after:bg-gradient-to-r after:from-[#42e1ac] after:via-[#e4e142] after:to-[#db42e1] after:transition-all after:duration-200 after:content-[''] {isOpen
				? 'rotate-[855deg] before:translate-y-0  before:rotate-90 before:bg-gradient-to-r before:from-[#42e1ac] before:via-[#e4e142] before:to-[#db42e1] after:invisible'
				: ''}"
		></div>
	</div>
</button>
