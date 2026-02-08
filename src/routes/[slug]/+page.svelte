<script lang="ts">
	import { error } from '@sveltejs/kit'
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

	const titles: Record<string, string> = {
		home: 'Home',
		contribute: 'Contribute',
		people: 'People',
		tech: 'Technology',
		deploy: 'Deployment',
		clubs: 'Club Websites',
		huts: 'Hut Booking',
		guides: 'Routes Database',
		himalayan_index: 'Himalayan Index',
		reporting: 'Route Reporting',
		topoeditor: 'TopoEditor',
		learnsvelte: 'Learn Svelte',
		bespoke: 'Bespoke',
		development: 'Development'
	}

	const pages: Record<string, string> = {
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
	}

	let slug = $derived(page.params.slug ?? '')
	let content = $derived(pages[slug])
	let title = $derived(titles[slug])

	$effect(() => {
		if (!content) error(404, 'Page not found')
	})
</script>

<svelte:head>
	{#if title}
		<title>{title} — Climbing and Mountaineering Software</title>
	{/if}
</svelte:head>

<div class="px-4 sm:px-8">
	<Markdown {content} />
</div>
