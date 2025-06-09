<script lang="ts">
	import Markdown from '$lib/Markdown.svelte'
	import home from '$lib/content/home.md?raw'
</script>

<div class="prose prose-a:no-underline m-2 max-w-none px-8">
	<Markdown content={home} />
</div>
