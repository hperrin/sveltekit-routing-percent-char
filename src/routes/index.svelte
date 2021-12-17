<script>
	const simpleSingle = `/${encodeURIComponent('my query')}/`;
	const simpleDouble = encodeURI(simpleSingle);
	const percentfulSingle = `/${encodeURIComponent('% is the percent sign')}/`;
	const percentfulDouble = encodeURI(percentfulSingle);
</script>

<h1>SvelteKit Routing Bug Demo</h1>
<p>Click on one of the links below, then refresh the page.</p>
<p>
	Simple query, single encoded: <a href={simpleSingle}><code>{simpleSingle}</code></a>
	<br />
	(Behavior: works on click, works on refresh)
</p>
<p>
	Simple query, double encoded: <a href={simpleDouble}><code>{simpleDouble}</code></a>
	<br />
	(Behavior: works on click, breaks on refresh)
</p>
<p>
	Percentful query, single encoded: <a href={percentfulSingle}><code>{percentfulSingle}</code></a>
	<br />
	(Behavior: breaks on click, works on refresh)
</p>
<p>
	Percentful query, double encoded: <a href={percentfulDouble}><code>{percentfulDouble}</code></a>
	<br />
	(Behavior: works on click, breaks on refresh)
</p>
