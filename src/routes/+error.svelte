<script lang="ts">
	import { page } from '$app/state'
</script>

<div class="px-4 py-16 text-center sm:px-8">
	<h1 class="mb-4 text-4xl font-bold">{page.status}</h1>
	<p class="text-lg text-gray-600">{page.error?.message ?? 'Page not found'}</p>
	<a href="/" class="text-camsblue mt-8 inline-block hover:underline">← Back to home</a>
</div>
