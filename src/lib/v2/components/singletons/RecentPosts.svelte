<script lang="ts">
	import BlogPostCard from '$lib/v2/components/molecules/BlogPostCard.svelte';
	import type { BlogPost } from '$lib/v2/utils/types';

	export let posts: BlogPost[];
</script>

<div class="container">
	<div class="grid">
		{#each posts as post}
			<BlogPostCard
				slug={post.slug}
				title={post.title}
				showImage={true}
				date={post.date}
				contributor={post.contributor}
				coverImage={post.coverImage}
			/>
		{/each}
	</div>
</div>

<style lang="scss">
	@import '$lib/scss/breakpoints.scss';

	.container {
		color: rgba(245, 245, 245, 0.8);
		background: rgba(26, 26, 26, 1);
	}

	.grid {
		padding-top: 3rem;
		width: 100%;
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-gap: 20px;
		padding-inline: 1.5rem;

		@include for-phone-only {
			grid-template-columns: 1fr;
		}

		@include for-tablet-landscape-up {
			grid-template-columns: 1fr 1fr;
		}

		@include for-desktop-up {
			grid-template-columns: 1fr 1fr 1fr;
		}
	}
</style>
