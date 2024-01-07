<script lang="ts">
	import { onMount } from 'svelte';
	import { animate, scroll } from 'motion';

	let word1 = 'MODERNITE';
	let word2 = 'EFFICACITE';

	onMount(() => {
		const items = document.querySelector('.slide  div') as HTMLDivElement;
		scroll(
			animate(
				items,
				{
					transform: [`translateX(-10vw)`]
				},
				{ easing: 'ease-in-out' }
			),
			{ target: document.querySelector('.slide') as HTMLDivElement }
		);
	});
</script>

<div class="slide">
	<div>
		{#each Array(10) as item}
			<span>
				{word1}
			</span>
			&nbsp;
			<span> - </span>
			&nbsp;
			<span>
				{word2}
			</span>
			&nbsp;
			<span> - </span>
			&nbsp;
		{/each}
	</div>

</div>

<style>
	.slide {
		position: relative;
		width: calc(100% - 10vw);
		/* background-color: red; */
		overflow: clip;
		border-radius: 100vw;
		margin-inline: 5vw;
		border: 2px solid var(--woodsmoke-500);
		padding: clamp(10px, 15px, 20px);
		flex-wrap: nowrap;
		display: flex;
		align-items: center;

	}
	
	
	.slide > div {
		flex-shrink: 0;
		flex-wrap: nowrap;
	}
	
	
	span {
		flex-shrink: 0;
		font-size: clamp(14px, 1.3vw + 0.1rem, 1.5rem);
		font-weight: 800;
	}

	@media (width < 700px) {
		.slide {
			padding: 10px;
		}
	}

	
</style>
