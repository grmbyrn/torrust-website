<script lang="ts">
	import '$lib/scss/global.scss';
	import type { Hst as HstType } from '@histoire/plugin-svelte';
	import Hero from './Hero.svelte';

	export let Hst: HstType;
</script>

<svelte:component this={Hst.Story} title="Organisms/Hero" layout={{ type: 'single', iframe: true }}>
	<Hero hasFeatures={true} hasPosts={true} />
</svelte:component>
