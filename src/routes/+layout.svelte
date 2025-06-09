<script lang="ts">
	import '../app.css'
	import Navbar from './NavBar.svelte'

	let { children } = $props()
</script>

<a href="#main" class="sr-only">Skip to main content</a>
<div class="flex h-screen w-screen flex-col justify-between bg-gray-50">
	<header>
		<Navbar />
	</header>
	<div class={`overflow-scroll-y mt-10 mb-auto flex md:mt-10 `}>
		<main id="main">
			{@render children()}
		</main>
	</div>
	<footer class="footer h-10 bg-gray-200">
		<hr class="border-1 border-gray-500 bg-gray-500" />
		<div class=" mx-10 my-2 flex justify-between text-sm">
			<span>
				© Nevil Hewitt {new Date().getFullYear()}
			</span>
		</div>
	</footer>
</div>
