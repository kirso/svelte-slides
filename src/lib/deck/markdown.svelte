<script lang="ts">
	export let name = 'example.md';
	export let external = false;
</script>

{#if external}
	<section data-markdown={name} />
{:else}
	<section data-markdown>
		<div class="data-template">
			<slot />
		</div>
	</section>
{/if}
