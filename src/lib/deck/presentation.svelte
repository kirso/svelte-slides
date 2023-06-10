<script lang="ts">
	import Slide from './slide.svelte';
	import Code from './code.svelte';
	import Markdown from './markdown.svelte';
	import Notes from './notes.svelte';
</script>

<Slide animate>
	<Code id="code" lines>
		{`
    function love() {}
  `}
	</Code>
</Slide>

<Slide animate>
	<Code id="code" lines>
		{`
    function love() {
      console.log('Love svelte')
    }

  `}
	</Code>
</Slide>

<Slide animate>
	<p class="uppercase">Transitions</p>

	<div class="flex gap-2 place-content-center">
		<div data-id="box1" class="w-[100px] h-[100px] bg-gray-400" />
		<div data-id="box2" class="w-[100px] h-[100px] bg-gray-400" />
		<div data-id="box3" class="w-[100px] h-[100px] bg-gray-400" />
	</div>
</Slide>
<Slide animate>
	<p class="uppercase">Transitions</p>

	<div class="flex gap-2 place-content-center">
		<div data-id="box1" class="w-[200px] h-[200px] bg-sky-400" />
		<div data-id="box2" class="w-[200px] h-[200px] bg-green-400" />
		<div data-id="box3" class="w-[200px] h-[200px] bg-teal-700" />
	</div>
</Slide>

<Slide animate>
	<h1>Slide</h1>
	<Notes>Notes</Notes>
</Slide>

<Markdown>
	{`
		## Markdown
		hello
	`}
</Markdown>

<Markdown name="example.md" external />

<Slide>
	<Code lines>
		{`
			function notLove() {
				console.log("SVELTE!")
			}
			`}
	</Code>
</Slide>
