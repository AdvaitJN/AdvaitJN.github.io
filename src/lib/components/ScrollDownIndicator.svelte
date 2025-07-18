<script lang="ts">
	import { onMount } from 'svelte';

	let isVisible = true;

	onMount(() => {
		const handleScroll = () => {
			console.log('Scroll event detected', window.scrollY < document.body.scrollHeight - 1500);
			isVisible = window.scrollY < document.body.scrollHeight - 1500;
		};

		window.addEventListener('scroll', handleScroll);
		return () => {
			window.removeEventListener('scroll', handleScroll);
		};
	});
</script>

{#if isVisible}
	<div class="scrolldown-bar">
		<span class="follow-text">SCROLL DOWN</span>
		<div class="vertical-arrow"></div>
	</div>
{/if}

<style lang="scss">
	/* Base styles (applied to all devices) */
	.scrolldown-bar {
		position: absolute;
		bottom: 0;
		left: 60px;
		display: flex;
		flex-direction: column;
		align-items: center;
		z-index: 1000;
		transition: display 0.3s;

		.follow-text {
			color: var(--primary-color);
			font-size: 1rem;
			writing-mode: vertical-rl;
		}

		.vertical-arrow {
			width: 2px;
			height: 200px;
			background-color: var(--primary-color);
			position: relative;
			margin: 37.5px auto;
		}

		.vertical-arrow::after {
			content: '';
			position: absolute;
			left: 50%;
			bottom: 0;
			transform: translateX(-50%) translateY(50%);
			border-left: 8px solid transparent;
			border-right: 8px solid transparent;
			border-top: 12px solid var(--primary-color); /* color of the arrowhead */
			width: 0;
			height: 0;
		}
	}

	/* Large screens (≥992px) */
	@media (min-width: 992px) {
		.scrolldown-bar {
			position: fixed;
		}
	}
</style>
