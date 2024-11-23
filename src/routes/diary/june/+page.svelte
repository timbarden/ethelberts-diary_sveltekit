<script>
	import MarkdownIt from "markdown-it";
	import MarkdownItFootnote from "markdown-it-footnote";
	import markdownContent from "$lib/content/entries/june/01.md?raw";

	const md = new MarkdownIt({
		html: true
	}).use(MarkdownItFootnote);
</script>

<svelte:head>
	<title>Ethelbert's Diary | June 1919</title>
	<meta
		data-key="description"
		name="description"
		content="June 1919 entries of the diary"
	/>
</svelte:head>

{@html md.render(markdownContent)}