<script lang="ts">
	import { marked } from 'marked'

	let {
		content
	}: {
		content: string | undefined
	} = $props()

	const renderer = {
		link: (href: any, _: undefined, title: string): string | false => {
			if (!href) return title
			if (typeof href === 'string') {
				if (!!href && href.includes('http')) {
					return `<a href="${href}" target="_blank" rel="noopener noreferrer">${title || href}</a>`
				} else {
					return `<a href="${href}">${title || href}</a>`
				}
			} else if (href.href) {
				if (!!href.href && href.href.includes('http')) {
					return `<a href="${href.href}" target="_blank" rel="noopener noreferrer">${title || href.text}</a>`
				} else {
					return `<a href="${href.href}">${title || href.text}</a>`
				}
			} else {
				return title
			}
		}
	} as any

	marked.use({ renderer })
</script>

<div class="markdown">
	{@html marked.parse(content || '')}
</div>

<style>
</style>
