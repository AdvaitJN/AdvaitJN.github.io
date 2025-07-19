<script lang="ts">
	import Button from '$lib/components/Button.svelte';
	import ContactForm from '$lib/components/ContactForm.svelte';
	import ScrollDownIndicator from '$lib/components/ScrollDownIndicator.svelte';
	import SectionHeader from '$lib/components/SectionHeader.svelte';
	import AboutMeSection from '$lib/components/sections/AboutMeSection.svelte';
	import ContactSection from '$lib/components/sections/ContactSection.svelte';
	import LandingSection from '$lib/components/sections/LandingSection.svelte';
	import ServicesSection from '$lib/components/sections/ServicesSection.svelte';
	import WorksSection from '$lib/components/sections/WorksSection.svelte';
	import SocialBar from '$lib/components/SocialBar.svelte';
	import '../app.css';
</script>

<div class="fixed">
	<SocialBar />
	<ScrollDownIndicator />
	<div class="fixed-letstalk-button">
		<a href="#contact" class="btn-link">
			<Button type="button">Let's Talk</Button>
		</a>
	</div>
</div>

<LandingSection />

<AboutMeSection />

<WorksSection />

<ServicesSection />

<ContactSection />

<style lang="scss">
	/* Base styles (applied to all devices) */
	.fixed-letstalk-button {
		position: fixed;
		top: 40px;
		right: 40px;
		z-index: 1000;
	}

	.btn-link {
		text-decoration: none;
	}

	/* Small screens (≥576px) */
	@media (min-width: 576px) {
		:global(html) {
			font-size: 14px;
		}
	}

	/* Medium screens (≥768px) */
	@media (min-width: 768px) {
		:global(html) {
			font-size: 16px;
		}
	}

	/* Large screens (≥992px) */
	@media (min-width: 992px) {
		:global(html) {
			font-size: 18px;
		}
	}

	/* Extra large screens (≥1200px) */
	@media (min-width: 1200px) {
		:global(html) {
			font-size: 20px;
		}
	}

	/* Extra extra large screens (≥1400px) */
	@media (min-width: 1400px) {
	}
</style>
