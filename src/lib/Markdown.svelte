<script lang="ts">
	import { marked, type RendererObject } from 'marked'

	let {
		content
	}: {
		content: string | undefined
	} = $props()

	const renderer: RendererObject = {
		link({ href, text }) {
			const inner = text?.startsWith('![')
				? marked.parseInline(text ?? '')
				: (text ?? '')
			if (href && href.startsWith('http')) {
				return `<a href="${href}" target="_blank" rel="noopener noreferrer">${inner}</a>`
			}
			return `<a href="${href}">${inner}</a>`
		}
	}

	marked.use({ renderer })
</script>

<div class="markdown">
	{@html marked.parse(content || '', { async: false })}
</div>

<style>
</style>
