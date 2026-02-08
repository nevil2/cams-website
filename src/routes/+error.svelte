<script lang="ts">
	import { page } from '$app/state'
</script>

<div class="px-4 sm:px-8 py-16 text-center">
	<h1 class="text-4xl font-bold mb-4">{page.status}</h1>
	<p class="text-lg text-gray-600">{page.error?.message ?? 'Page not found'}</p>
	<a href="/" class="mt-8 inline-block text-camsblue hover:underline">← Back to home</a>
</div>
