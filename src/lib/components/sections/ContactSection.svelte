<script lang="ts">
	import SectionHeader from '$lib/components/SectionHeader.svelte';
</script>

<div id="contact" class="container contact">
	<SectionHeader title="CONTACT ME" />
	<div class="wrapper">
		<div class="contact-details">
			<h2>Let's Connect!</h2>
			<p>
				Have a project in mind or just want to say hello? Whether you're looking to build something
				new, solve a problem, or explore how technology can make a difference for you, I'd love to
				hear from you.
			</p>
			<p>
				You can reach me at:
				<a href="mailto:hi@advaitjn.dev">hi@advaitjn.dev</a>
			</p>
			<p>
				Or connect with me via
				<a
					href="https://linkedin.com/in/advaitjn"
					target="_blank"
					rel="noopener noreferrer"
				>
					LinkedIn
				</a>
			</p>
		</div>
		<div class="contact-image-wrap" role="img" aria-label="Contact">
			<svg
				class="contact-illustration"
				xmlns="http://www.w3.org/2000/svg"
				viewBox="0 0 811.453 311.372"
				aria-hidden="true"
			>
				<title>Contact</title>
				<g transform="translate(-411.975 -357.501)">
					<path
						d="M831.938,243.782a48.214,48.214,0,0,1,48.147-45.694c1.465,0,2.912.076,4.344.2a64.058,64.058,0,0,1,110.733-.052c1.208-.091,2.424-.152,3.656-.152a48.214,48.214,0,0,1,48.147,45.693"
						transform="translate(-419.962 207.558)"
						fill="var(--primary-color)"
						opacity="0.12"
					/>
					<path
						d="M844.569,239.117a48.214,48.214,0,0,1,48.147-45.694c1.465,0,2.912.076,4.344.2a64.058,64.058,0,0,1,110.733-.052c1.208-.091,2.424-.152,3.656-.152a48.214,48.214,0,0,1,48.147,45.693"
						transform="translate(-422.552 208.515)"
						fill="none"
						stroke="currentColor"
						stroke-miterlimit="10"
						stroke-width="1"
						opacity="0.35"
					/>
					<path
						d="M155.988,539.473A159.577,159.577,0,0,1,315.344,388.236c4.85,0,9.639.253,14.379.677a212.017,212.017,0,0,1,366.5-.173c4-.3,8.024-.5,12.1-.5A159.577,159.577,0,0,1,867.679,539.473"
						transform="translate(322.013 86.835)"
						fill="var(--primary-color)"
						opacity="0.12"
					/>
					<path
						d="M197.794,524.033A159.577,159.577,0,0,1,357.15,372.8c4.85,0,9.639.253,14.379.677a212.017,212.017,0,0,1,366.5-.173c4-.3,8.024-.5,12.1-.5A159.577,159.577,0,0,1,909.485,524.033"
						transform="translate(313.444 90)"
						fill="none"
						stroke="currentColor"
						stroke-miterlimit="10"
						stroke-width="1"
						opacity="0.35"
					/>
					<path
						d="M84.962,212.741a65.236,65.236,0,0,1,65.146-61.827c1.983,0,3.94.1,5.878.277a86.674,86.674,0,0,1,149.827-.071c1.635-.123,3.28-.206,4.946-.206a65.236,65.236,0,0,1,65.146,61.825"
						transform="translate(493.985 456.133)"
						fill="currentColor"
					/>
					<path
						d="M102.053,206.428A65.236,65.236,0,0,1,167.2,144.6c1.983,0,3.94.1,5.878.277a86.674,86.674,0,0,1,149.828-.071c1.635-.123,3.28-.206,4.946-.206A65.236,65.236,0,0,1,393,206.427"
						transform="translate(490.482 457.427)"
						fill="none"
						stroke="currentColor"
						stroke-miterlimit="10"
						stroke-width="1"
						opacity="0.5"
					/>
				</g>
			</svg>
		</div>
	</div>
</div>

<style lang="scss">
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
		flex-direction: column;
		padding-top: 37.5px;
		gap: 24px;
	}

	.contact-details {
		h2 {
			font-size: 2rem;
			color: var(--secondary-color);
			font-weight: bold;
			margin-bottom: 1rem;
		}

		p {
			margin-bottom: 1rem;
			line-height: 1.6;

			&:last-child {
				margin-bottom: 0;
			}
		}
	}

	.contact-image-wrap {
		display: flex;
		align-items: center;
		justify-content: center;
		border-radius: 1rem;
		overflow: hidden;
	}

	.contact-illustration {
		width: 100%;
		height: auto;
		display: block;
		color: var(--secondary-color);
	}

	@media (min-width: 992px) {
		.wrapper {
			height: calc(100% - 100px);
			margin: 0 60px;
			flex-direction: row;
			gap: 20px;
		}

		.contact-details,
		.contact-image-wrap {
			flex: 1 1 0;
		}

		.contact-illustration {
			max-height: 320px;
		}
	}

	@media (min-width: 1200px) {
		.wrapper {
			margin: 0 80px;
		}
	}
</style>
