<script lang="ts">
	import { page } from '$app/state'
	import Markdown from '$lib/Markdown.svelte'
	import home from '$lib/content/home.md?raw'
	import contribute from '$lib/content/contribute.md?raw'
	import about from '$lib/content/about.md?raw'
	import tech from '$lib/content/tech.md?raw'
	import deploy from '$lib/content/deploy.md?raw'
	import clubs from '$lib/content/clubwebsites.md?raw'
	import huts from '$lib/content/hutbooking.md?raw'
	import guides from '$lib/content/digitalguide.md?raw'
	import himalayan_index from '$lib/content/himalayanindex.md?raw'
	import reporting from '$lib/content/routereporting.md?raw'
	import topoeditor from '$lib/content/topoeditor.md?raw'
	import learnsvelte from '$lib/content/svelte.md?raw'

	let content = $derived(
		{
			home,
			contribute,
			about,
			tech,
			deploy,
			clubs,
			huts,
			guides,
			himalayan_index,
			reporting,
			topoeditor,
			learnsvelte
		}[page.params.slug]
	)
</script>

<div class="prose prose-a:no-underline m-2 max-w-none px-8">
	<Markdown {content} />
</div>
