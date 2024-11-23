<script>
	import MarkdownIt from "markdown-it";
	import markdownContent from "$lib/content/entries/test.md?raw";

	const md = new MarkdownIt({
		html: true
	});
</script>

<svelte:head>
	<title>Ethelbert's Diary | About</title>
	<meta
		data-key="description"
		name="description"
		content="Some background and context to the diary."
	/>
</svelte:head>

{@html md.render(markdownContent)}