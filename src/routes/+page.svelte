<script lang="ts">
	import Markdown from '$lib/Markdown.svelte'
	import home from '$lib/content/home.md?raw'
</script>

<div class="px-4 sm:px-8">
	<Markdown content={home} />
</div>
