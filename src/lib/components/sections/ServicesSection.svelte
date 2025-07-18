<script>
	import SectionHeader from '../SectionHeader.svelte';

	const services = [
		{
			icon: '📱',
			title: 'Mobile App Development',
			description:
				'Build modern, high-performance mobile applications for iOS and Android using React Native and Flutter.'
		},
		{
			icon: '🌐',
			title: 'Web Application Development',
			description:
				'Create secure, scalable web applications with robust frontends and powerful backends.'
		},
		{
			icon: '💻',
			title: 'Desktop App Development',
			description:
				'Develop cross-platform desktop applications with reliable performance and smooth UX.'
		},
		{
			icon: '🔗',
			title: 'API Design & Integration',
			description:
				'Design, develop, and integrate RESTful APIs that connect your products and services.'
		},
		{
			icon: '☁️',
			title: 'Cloud Integration & Consulting',
			description:
				'Migrate, deploy, and optimize your systems in the cloud with AWS, GCP, and Firebase.'
		},
		{
			icon: '🤖',
			title: 'AI & Computer Vision Solutions',
			description:
				'Implement AI-powered features and computer vision systems for automation and real-time analysis.'
		}
	];
</script>

<div class="container">
	<SectionHeader title="SERVICES" base="background" />
	<div class="wrapper">
		<div class="grid">
			{#each services as service}
				<div class="widget">
					<div class="icon">{service.icon}</div>
					<div class="title">{service.title}</div>
					<div class="desc">{service.description}</div>
				</div>
			{/each}
		</div>
	</div>
</div>

<style>
	/* Base styles (applied to all devices) */
	.container {
		padding: 40px;
		height: auto;
	}

	.wrapper {
		display: flex;
		height: calc(100% - 100px);
		flex-direction: column;
		padding-top: 37.5px;
	}

	.grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
		gap: 2rem;
	}
	.widget {
		background: var(--background2-color);
		border-radius: 1.5rem;
		box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
		padding: 2rem 1.5rem 1.5rem 1.5rem;
		display: flex;
		flex-direction: column;
		align-items: center;
		transition:
			box-shadow 0.2s,
			border 0.2s;
		border: 2px solid transparent;
		/* min-height: 260px; */
		position: relative;
	}
	.widget:hover,
	.widget:focus-visible {
		border: 2px solid var(--secondary-color);
		box-shadow: 0 6px 24px rgba(206, 135, 42, 0.18);
		z-index: 1;
	}
	.icon {
		font-size: 2.5rem;
		margin-bottom: 1rem;
		background: var(--background-color);
		border-radius: 1rem;
		padding: 1rem;
		color: var(--secondary-color);
		box-shadow: 0 1px 4px rgba(206, 135, 42, 0.13);
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.title {
		font-size: 1.15rem;
		font-weight: 600;
		color: var(--primary-color);
		margin-bottom: 0.5rem;
		text-align: center;
		letter-spacing: 0.01em;
	}
	.desc {
		font-size: 0.96rem;
		color: #dbdbdb;
		text-align: center;
		margin-top: 0.25rem;
		line-height: 1.5;
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
			margin: 0px 60px;
		}
	}

	/* Extra large screens (≥1200px) */
	@media (min-width: 1200px) {
		.wrapper {
			margin: 0px 80px;
		}
		.grid {
			grid-template-columns: repeat(3, 1fr);
		}
	}

	/* Extra extra large screens (≥1400px) */
	@media (min-width: 1400px) {
	}
</style>
