<script lang="ts">
	import '$lib/scss/global.scss';
	import type { Hst as HstType } from '@histoire/plugin-svelte';
	import FeatureCard from './FeatureCard.svelte';

	export let Hst: HstType;
</script>

<svelte:component this={Hst.Story} title="Molecules/Feature Card">
	<div style="padding: 12px;">
		<svelte:component this={Hst.Variant} title="Default">
			<FeatureCard
				name="Feature Name"
				description="Doggo ipsum very taste wow doge noodle horse wow very biscit, woofer. Puggorino you are doin me a concern long doggo woofer borkdrive length boy, shoob long water shoob ur givin me a spook."
				image="https://placedog.net/500"
				tags={[{ label: 'Wow!' }, { label: 'Very cool!', color: 'secondary' }]}
			/>
		</svelte:component>
	</div>
</svelte:component>
