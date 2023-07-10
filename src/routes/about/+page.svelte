<script>
	import { Avatar } from '@skeletonlabs/skeleton';
	import { slide, fade } from 'svelte/transition';

	export let visible = false;

	const changeAlert = () => {
		visible = !visible;
	};
</script>

<div class="container mx-auto p-8 space-y-8">
	<h1 class="h1">Hello Doctor</h1>
	<p>This is a utility driven website for fast and practical support for medical students</p>
	<section>
		<a class="btn variant-filled-primary" href="https://kit.svelte.dev/">SvelteKit</a>
		<a class="btn variant-filled-secondary" href="https://tailwindcss.com/">Tailwind</a>
		<a class="btn variant-filled-tertiary" href="https://github.com/">GitHub</a>
		<button class="btn variant-filled-tertiary" on:click={changeAlert} />
	</section>
	{#if visible}
		<aside class="alert variant-filled-error" transition:fade|local={{ duration: 200 }}>
			<!-- Icon -->
			<div>teste div 1</div>
			<!-- Message -->
			<div class="alert-message">
				<h3 class="h3">TITLE</h3>
				<p>placeholder</p>
			</div>
			<!-- Actions -->
			<div class="alert-actions"><button class="btn variant-filled-primary" /></div>
		</aside>
	{/if}

</div>
