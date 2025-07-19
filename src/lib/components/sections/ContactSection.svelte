<script lang="ts">
	import ContactForm from '$lib/components/ContactForm.svelte';
	import SectionHeader from '$lib/components/SectionHeader.svelte';
</script>

<div id="contact" class="container contact">
	<SectionHeader title="CONTACT ME" />
	<div class="wrapper">
		<div class="contact-details">
			<h2>Let's Connect!</h2>
			<br />
			<p>
				Have a project in mind or just want to say hello? Whether you’re looking to build something
				new, solve a problem, or explore how technology can make a difference for you, I’d love to
				hear from you. Fill out the form and I’ll get back to you as soon as possible!
			</p>
			<br />
			<p>
				You can reach me at: <a href="mailto:advaitjayadevannair@gmail.com"
					>advaitjayadevannair@gmail.com</a
				>
			</p>
			<br />
			<p>
				Or connect with me via <a
					href="https://linkedin.com/in/advaitjn"
					target="_blank"
					rel="noopener noreferrer">LinkedIn</a
				>
			</p>
		</div>
		<div class="contact-form">
			<ContactForm />
		</div>
	</div>
</div>

<style lang="scss">
	/* Base styles (applied to all devices) */
	.container {
		padding: 40px;
		height: auto;
	}
	.contact {
		background-color: var(--background2-color);
		a {
			color: var(--secondary-color);
			font-weight: 600;
			text-decoration: none;
			transition:
				color 0.18s,
				border-bottom 0.18s;
			border-bottom: 2px solid transparent;
			padding-bottom: 2px;
		}

		a:hover,
		a:focus {
			color: #db9b4c;
			border-bottom: 2px solid #ce872a;
			outline: none;
		}
	}

	.wrapper {
		display: flex;
		height: calc(100% - 100px);
		flex-direction: column;
		padding-top: 37.5px;
		gap: 37.5px;
	}

	.contact-details {
		flex: 0 0 40%;
	}

	.contact-form {
		flex: 0 0 60%;
	}

	.contact-details {
		h2 {
			font-size: 2rem;
			color: var(--secondary-color);
			font-weight: bold;
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
			display: flex;
			height: calc(100% - 100px);
			margin: 0px 60px;
			flex-direction: row;
			gap: 20px;
		}
	}

	/* Extra large screens (≥1200px) */
	@media (min-width: 1200px) {
		.wrapper {
			margin: 0px 80px;
		}
	}

	/* Extra extra large screens (≥1400px) */
	@media (min-width: 1400px) {
	}
</style>
