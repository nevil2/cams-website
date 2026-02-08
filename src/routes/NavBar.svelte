<script lang="ts">
	let navbarOpen = $state(false)
	const toggleNavbarOpen = () => {
		navbarOpen = !navbarOpen
	}
</script>

{#snippet links()}
	<a class="text-gray-200 hover:text-white" href="/guides" onclick={() => navbarOpen = false}>Routes Database</a>
	<a class="text-gray-200 hover:text-white" href="/clubs" onclick={() => navbarOpen = false}>Club Websites</a>
	<a class="text-gray-200 hover:text-white" href="/bespoke" onclick={() => navbarOpen = false}>Bespoke</a>
	<a class="text-gray-200 hover:text-white" href="/development" onclick={() => navbarOpen = false}>Development</a>
	<a class="text-gray-200 hover:text-white" href="/tech" onclick={() => navbarOpen = false}>Technology</a>
	<a class="text-gray-200 hover:text-white" href="/deploy" onclick={() => navbarOpen = false}>Deployment</a>
{/snippet}

<nav class="bg-camsblue fixed top-0 z-50 w-full py-1 text-gray-50">
	<div class="container mx-auto max-w-5xl px-4 sm:px-8">
		<div class="flex items-center justify-between">
			<a class="flex items-center text-lg text-gray-200 hover:text-white" href="/">Home</a>
			<button
				type="button"
				class="inline-flex h-10 items-center rounded-lg p-2 text-sm text-gray-500 bg-camsblue appearance-none border-0  focus:ring-2 focus:ring-gray-200 focus:outline-none sm:hidden"
				aria-expanded={navbarOpen}
				aria-controls="mobile-menu"
				onclick={toggleNavbarOpen}
			>
				<span class="sr-only">{navbarOpen ? 'Close main menu' : 'Open main menu'}</span>
				<svg
					class="h-6 w-6"
					aria-hidden="true"
					fill="currentColor"
					viewBox="0 0 20 20"
					xmlns="http://www.w3.org/2000/svg"
				>
					<path
						fill-rule="evenodd"
						d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
						clip-rule="evenodd"
					/>
				</svg>
			</button>
			<div class="hidden sm:ml-auto sm:flex">
				<div class="flex flex-row gap-6">
					{@render links()}
				</div>
			</div>
		</div>
		{#if navbarOpen}
			<div id="mobile-menu" class="mt-2 flex flex-col space-y-2 sm:hidden">
				{@render links()}
			</div>
		{/if}
	</div>
</nav>
