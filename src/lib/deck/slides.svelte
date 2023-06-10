<script lang="ts">
	import Reveal from 'reveal.js';
	import Markdown from 'reveal.js/plugin/markdown/markdown';
	import Highlight from 'reveal.js/plugin/highlight/highlight';
	import Notes from 'reveal.js/plugin/notes/notes';
	import 'reveal.js/dist/reveal.css';
	import 'reveal.js/dist/theme/night.css';
	import 'reveal.js/plugin/highlight/zenburn.css';

	import Presentation from './presentation.svelte';
	import { onMount } from 'svelte';

	onMount(() => {
		const deck = new Reveal({
			autoAnimateEasing: 'ease',
			autoAnimateDuration: 1,
			hash: true,
			controls: true,
			progress: true
		});

		deck.initialize({
			plugins: [Markdown, Highlight, Notes]
		});
	});
</script>

<div class="reveal">
	<div class="slides">
		<Presentation />
	</div>
</div>
