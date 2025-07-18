<script lang="ts">
	export let title: string;
	export let accentWidth: string = '25%'; // Width for accent line, e.g. '30%'
	export let base: 'base' | 'background' = 'base'; // Choose line color type
</script>

<div class="section-header">
	<h1>{title}</h1>
	<div class="line-wrapper">
		<div class="line {base}"></div>
		<div class="line accent" style="left: {accentWidth}; right: {accentWidth};"></div>
	</div>
</div>

<style>
	.section-header {
		text-align: center;
		position: relative;

		h1 {
			color: var(--primary-color);
			font-weight: bold;
			margin-bottom: 8px;
			font-size: 1.5rem;
		}

		.line-wrapper {
			position: relative;
			width: 400px;
			margin: 0 auto;
			height: 8px;
		}

		.line.base {
			position: absolute;
			left: 0;
			right: 0;
			top: 50%;
			height: 4px;
			background: var(--background-color);
			border-radius: 4px;
			transform: translateY(-50%);
			z-index: 1;
		}

		.line.background {
			position: absolute;
			left: 0;
			right: 0;
			top: 50%;
			height: 4px;
			background: var(--background2-color);
			border-radius: 4px;
			transform: translateY(-50%);
			z-index: 1;
		}

		.line.accent {
			position: absolute;
			left: 30%;
			right: 30%;
			top: 50%;
			height: 4px;
			background: var(--secondary-color);
			border-radius: 4px;
			transform: translateY(-50%);
			z-index: 2;
		}
	}
</style>
