<script>
	import HeaderMenu from '$lib/components/HeaderMenu.svelte';
	import brainWave from '$assets/brainwave.svg';
	import BrainBtn from '$lib/components/BrainBtn.svelte';
	import { navigation } from '$lib/constants';
	import { page } from '$app/stores';
	let { children } = $props();
</script>

{#snippet Header(image)}
	<div class="h-[5rem] fixed top-0 left-0 w-full z-50 border-b border-gray-700 backdrop-blur-sm">
		<div class="size-full flex items-center justify-between px-7">
			<a href="/" class="md:pr-5">
				<img src={image} alt="Brain Wave" />
			</a>
			<nav class="flex justify-center items-center gap-7 md:hidden text-xs">
				{#each navigation as navElement}
					{#if navElement.onlyMobile == false}
						<a
							href={navElement.url}
							id={navElement.id}
							class="{$page.url.hash == navElement.url
								? 'text-white'
								: ''} uppercase text-gray-400 hover:text-white transition-colors"
							>{navElement.title}
						</a>
					{/if}
				{/each}
			</nav>
			<!-- account related things -->
			<div class="flex gap-7 items-center">
				<a
					href="#signup"
					class="uppercase text-sm text-gray-400 md:hidden font-semibold hover:text-white transition-colors"
				>
					new account
				</a>
				<BrainBtn title="sign in" ancher="#signin" />
			</div>
		</div>
	</div>
	<HeaderMenu />
{/snippet}

{@render Header(brainWave)}
{@render children()}
