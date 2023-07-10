<script lang="ts">
	// The ordering of these imports is critical to your app working properly
	//import '@skeletonlabs/skeleton/themes/theme-skeleton.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
	import { AppShell, AppBar, LightSwitch } from '@skeletonlabs/skeleton';
	import src from '$lib/assets/logo.svg';
</script>
<!-- App Shell -->
<AppShell slotSidebarLeft="bg-surface-500/5 w-56 p-4">
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<img {src} alt="heyhey" class="max-h-8 max-w-8">
				<strong class="text-xl uppercase">Med-Hub</strong>

			</svelte:fragment>
			<svelte:fragment slot="trail">
				<LightSwitch/>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://github.com/PedroTurik/SkeletonApp"
					target="_blank"
					rel="noreferrer"
				>
					GitHub
				</a>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<svelte:fragment slot="sidebarLeft">
		<!-- Insert the list: -->
			<nav class="list-nav">
				<ul>
					<li><a class="btn variant-filled-primary" href="/">Home</a></li>
					<li><a class="btn variant-filled-primary" href="/about">About</a></li>
				</ul>
			</nav>
		<!-- --- -->
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>
