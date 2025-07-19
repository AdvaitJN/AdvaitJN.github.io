<div class="container headshot-background">
	<nav>
		<h1>AdvaitJN</h1>
		<ul class="nav-links">
			<li><a href="/">Home</a></li>
			<li><a href="#about">About</a></li>
			<li><a href="#works">Works</a></li>
			<li><a href="#services">Services</a></li>
			<li><a href="/AdvaitJayadevanNairResumeSU25.pdf" target="_blank">Resume</a></li>
			<li><a href="#contact">Contact</a></li>
		</ul>
		<div></div>
	</nav>
	<div class="hero">
		<div>
			<p>Currently available for full time or freelance work</p>
			<h1>Full-Stack Web Developer</h1>
			<div></div>
		</div>
	</div>
</div>

<style lang="scss">
	/* Base styles (applied to all devices) */
	.nav-links {
		display: none;
	}

	.headshot-background {
		background-image: url('/images/headshot.png');
		background-repeat: no-repeat;
		background-position: bottom left;
		background-size: 100vh auto;
	}

	.container {
		padding: 40px;
		height: auto;
	}

	.hero {
		display: flex;
		flex-direction: column;
		justify-content: center;
		height: calc(100vh - 135px);
		padding-left: 10%;
		text-align: left;

		div {
			display: flex;
			flex-direction: column;
		}

		p {
			font-size: 1rem;
			flex: 1;
			width: 12rem;
			padding-bottom: 10px;
			border-bottom: 3px solid var(--secondary-color);
		}

		h1 {
			flex: 2;
			font-size: 5rem;
			width: 95%;
			color: var(--primary-color);
		}
	}

	nav {
		display: flex;
		justify-content: space-between;
		align-items: center;
		width: 100%;
		height: 55px;

		h1 {
			font-size: 2rem;
			flex: 1;
		}

		ul {
			list-style: none;
			display: flex;
			gap: 40px;

			li {
				a {
					text-decoration: none;
					color: var(--primary-color);
					font-weight: bold;

					&:hover {
						color: var(--secondary-color);
					}
				}
			}
		}

		div {
			flex: 1;
		}
	}

	/* Small screens (≥576px) */
	@media (min-width: 576px) {
	}

	/* Medium screens (≥768px) */
	@media (min-width: 768px) {
		.hero {
			h1 {
				width: 60%;
				color: var(--primary-color);
			}
		}
	}

	/* Large screens (≥992px) */
	@media (min-width: 992px) {
		.nav-links {
			display: flex;
		}
		.headshot-background {
			background-position: bottom right;
			background-size: auto calc(0.95 * 100vh);
		}
	}

	/* Extra large screens (≥1200px) */
	@media (min-width: 1200px) {
	}

	/* Extra extra large screens (≥1400px) */
	@media (min-width: 1400px) {
	}
</style>
