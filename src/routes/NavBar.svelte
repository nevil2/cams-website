<script lang="ts">
	let navbarOpen = false
	const toggleNavbarOpen = () => {
		navbarOpen = !navbarOpen
	}
</script>

<nav class="bg-camsblue text-camsneutral fixed top-0 z-50 flex min-h-10 w-screen">
	<div class="container mx-auto flex max-w-screen-lg items-center justify-between px-8">
		<div class="relative flex w-full justify-between sm:static sm:block sm:w-auto sm:justify-start">
			<a class="flex items-center" href="/">
				<span class="mr-6 hidden text-lg hover:text-white md:flex">Home</span>
				<span class="flex text-lg hover:text-white md:hidden">Home</span>
			</a>
			<button
				type="button"
				class="mt-5 ml-3 inline-flex h-10 items-center rounded-lg p-2 text-sm text-gray-500 hover:bg-gray-100 focus:ring-2 focus:ring-gray-200 focus:outline-none sm:hidden dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
				on:click={toggleNavbarOpen}
			>
				<span class="sr-only">Open main menu</span>
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
		</div>
		<div
			class={'flex-grow items-center sm:flex' + (navbarOpen ? ' flex' : ' hidden')}
			id="navbar-default"
		>
			<div class="flex flex-col sm:ml-auto sm:flex-row">
				<a href="/guides">Digital Guide</a>
				<a href="/reporting">Route Reporting</a>
				<a href="/topoeditor">TopoEditor</a>
				<a href="/clubs">Club Websites</a>
				<!-- <a href="/huts">Hut Booking</a> -->
				<!-- <a href="/himalayan_index">Himalayan Index</a> -->
				<a href="/about">About</a>
				<a href="/contribute">Contribute</a>
				<a href="/tech">Technology</a>
				<a href="/deploy">Deployment</a>
			</div>
		</div>
	</div>
</nav>

<style>
	.navbar {
		background-color: #5375e5;
		color: #e3e6f2;
	}
</style>
