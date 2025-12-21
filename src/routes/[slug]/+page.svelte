<script lang="ts">
	import { page } from '$app/state'
	import Markdown from '$lib/Markdown.svelte'
	import home from '$lib/content/home.md?raw'
	import contribute from '$lib/content/contribute.md?raw'
	import people from '$lib/content/people.md?raw'
	import tech from '$lib/content/tech.md?raw'
	import deploy from '$lib/content/deploy.md?raw'
	import clubs from '$lib/content/clubwebsites.md?raw'
	import huts from '$lib/content/hutbooking.md?raw'
	import guides from '$lib/content/digitalguide.md?raw'
	import himalayan_index from '$lib/content/himalayanindex.md?raw'
	import reporting from '$lib/content/routereporting.md?raw'
	import topoeditor from '$lib/content/topoeditor.md?raw'
	import learnsvelte from '$lib/content/svelte.md?raw'
	import bespoke from '$lib/content/bespoke.md?raw'
	import development from '$lib/content/development.md?raw'

	let content = $derived(
		{
			home,
			contribute,
			people,
			tech,
			deploy,
			clubs,
			huts,
			guides,
			himalayan_index,
			reporting,
			topoeditor,
			learnsvelte,
			bespoke,
			development
		}[page.params.slug || '']
	)
</script>

<div class="prose prose-a:no-underline max-w-none px-4 sm:px-8">
	<Markdown {content} />
</div>
