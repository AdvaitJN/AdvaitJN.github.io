<script lang="ts">
	import SectionHeader from '../SectionHeader.svelte';
	import Button from '../Button.svelte';
</script>

<div class="container">
	<SectionHeader title="WORKS" base="background" />
	<div class="wrapper">
		<div class="showcase">
			<img src="/images/showcase/aircraft-monitoring.png" alt="Aircraft Monitoring Showcase" />
		</div>
		<div class="details">
			<h2>Satellite Imagery Analysis for Aircraft Monitoring</h2>
			<h3>React | NEXT.js | YOLOv8 | ONNX | Google Maps Platform</h3>
			<br />
			<p>
				As part of a computer vision AI research project, I designed and implemented a computer
				vision pipeline to detect aircraft in satellite imagery using YOLOv8 and custom-trained
				models on aerial datasets. By applying data augmentation and performance tuning techniques,
				I was able to improve detection accuracy and model precision for real-time analysis
				scenarios. Through this work, I contributed to geospatial research initiatives focused on
				advancing surveillance automation and aircraft monitoring using satellite imagery.
			</p>
			<br />
			<Button
				type="button"
				on:click={() => {
					window.scrollTo({ top: document.body.scrollHeight, behavior: 'smooth' });
				}}
			>
				See More
			</Button>
		</div>
	</div>
	<div class="wrapper">
		<div class="showcase">
			<img src="/images/showcase/aircraft-monitoring.png" alt="Aircraft Monitoring Showcase" />
		</div>
		<div class="details">
			<h2>Satellite Imagery Analysis for Aircraft Monitoring</h2>
			<h3>React | NEXT.js | YOLOv8 | ONNX | Google Maps Platform</h3>
			<br />
			<p>
				As part of a computer vision AI research project, I designed and implemented a computer
				vision pipeline to detect aircraft in satellite imagery using YOLOv8 and custom-trained
				models on aerial datasets. By applying data augmentation and performance tuning techniques,
				I was able to improve detection accuracy and model precision for real-time analysis
				scenarios. Through this work, I contributed to geospatial research initiatives focused on
				advancing surveillance automation and aircraft monitoring using satellite imagery.
			</p>
			<br />
			<Button
				type="button"
				on:click={() => {
					window.scrollTo({ top: document.body.scrollHeight, behavior: 'smooth' });
				}}
			>
				See More
			</Button>
		</div>
	</div>
</div>

<style lang="scss">
	/* Base styles (applied to all devices) */
	.container {
		padding: 40px;
		height: auto;
	}

	.wrapper {
		display: flex;
		height: calc(100% - 100px);
		flex-direction: column;
		// padding-top: 37.5px;
	}

	.details {
		flex: 0 0 40%;
		padding-top: 37.5px;
		h2 {
			font-size: 2rem;
			color: var(--secondary-color);
			font-weight: bold;
		}
		h3 {
			font-size: 1rem;
			color: #999999;
			font-weight: bold;
		}
	}
	.showcase {
		width: 98%;
		padding-left: 1%;
		padding-right: 1%;
		flex: 0 0 60%;
		padding-top: 37.5px;

		img {
			width: 100%;
			height: 100%;
			object-fit: cover;
			border-radius: 1rem;
			box-shadow: 0 4px 24px 0 rgba(0, 0, 0, 0.4);
		}
	}

	/* Small screens (≥576px) */
	@media (min-width: 576px) {
	}

	/* Medium screens (≥768px) */
	@media (min-width: 768px) {
	}

	/* Large screens (≥992px) */
	@media (min-width: 992px) {
		.wrapper {
			padding: 0 60px;
		}
	}

	/* Extra large screens (≥1200px) */
	@media (min-width: 1200px) {
		.wrapper {
			display: flex;
			height: calc(100% - 100px);
			margin: 0px 80px;
			flex-direction: row;
			gap: 20px;
		}
		.wrapper:nth-of-type(even) {
			flex-direction: row-reverse;
		}
	}

	/* Extra extra large screens (≥1400px) */
	@media (min-width: 1400px) {
	}
</style>
