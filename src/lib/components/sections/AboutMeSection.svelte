<script lang="ts">
	import SectionHeader from '../SectionHeader.svelte';
	import SkillWidget from '../SkillWidget.svelte';
	import Button from '../Button.svelte';
</script>

<div class="container about">
	<SectionHeader title="ABOUT ME" />
	<div class="wrapper">
		<div class="aboutme">
			<h2>Hi There! I'm Advait Jayadevan Nair</h2>
			<h3>Software Engineer | Computer Vision Engineer | Full-Stack Developer</h3>
			<br />
			<p>
				I graduated with a Bachelor of Science in Computer Science Engineering from The Ohio State
				University, specializing in Artificial Intelligence. As an AWS Certified Solutions
				Architect, I combine cloud expertise with a passion for building innovative, impactful
				software solutions.
			</p>
			<br />
			<p>
				My experience includes developing inventory management tools and payroll/accounting
				management systems to drive organizational efficiency, as well as contributing to advanced
				AI projects in computer vision such as autonomous UAV software and satellite-based aircraft
				monitoring. I am highly skilled in modern web technologies, cloud architecture, and computer
				vision frameworks.
			</p>
			<br />
			<p>
				I thrive in collaborative environments and have a proven track record of leading technical
				teams, mentoring peers, and delivering solutions that make a tangible difference. I look
				forward to helping you achieve your goals by leveraging cutting-edge technology and my
				commitment to delivering results that matter.
			</p>
			<br />
			<Button
				type="button"
				on:click={() => {
					window.scrollTo({ top: document.body.scrollHeight, behavior: 'smooth' });
				}}>Resume</Button
			>
		</div>
		<div class="skills">
			<h4>SKILLS</h4>
			<div class="skill-grid">
				<SkillWidget imgSrc="/images/skills/typescript-96.png" name="TypeScript" color="#3178c6" />
				<SkillWidget imgSrc="/images/skills/aws-96.png" name="AWS" color="#eba02b" />
				<SkillWidget imgSrc="/images/skills/css3-96.png" name="CSS" color="#0078c0" />
				<SkillWidget imgSrc="/images/skills/docker-96.png" name="Docker" color="#2395ed" />
				<SkillWidget imgSrc="/images/skills/firebase-96.png" name="Firebase" color="#fec400" />
				<SkillWidget imgSrc="/images/skills/git-96.png" name="Git" color="#f7501b" />
				<SkillWidget imgSrc="/images/skills/html5-96.png" name="HTML" color="#e75000" />
				<SkillWidget imgSrc="/images/skills/java-96.png" name="Java" color="#339933" />
				<SkillWidget imgSrc="/images/skills/javascript-96.png" name="JavaScript" color="#f0db4f" />
				<SkillWidget imgSrc="/images/skills/nodejs-96.png" name="Node.js" color="#21a566" />
				<SkillWidget imgSrc="/images/skills/python-96.png" name="Python" color="#306998" />
				<SkillWidget imgSrc="/images/skills/react-96.png" name="React" color="#61DAFB" />
				<SkillWidget imgSrc="/images/skills/sql-96.png" name="SQL" color="#195cb6" />
			</div>
			<h4>CERTIFICATIONS</h4>
			<div class="skill-grid">
				<SkillWidget imgSrc="/images/skills/javascript-96.png" name="JavaScript" color="#f0db4f" />
				<SkillWidget imgSrc="/images/skills/typescript.png" name="TypeScript" color="#3178c6" />
			</div>
		</div>
	</div>
</div>

<style lang="scss">
	/* Base styles (applied to all devices) */
	.container {
		padding: 40px;
		height: auto;
	}

	.about {
		background-color: var(--background2-color);
	}

	.wrapper {
		display: flex;
		height: calc(100% - 100px);
		flex-direction: column;
		padding-top: 37.5px;
	}

	.skills {
		h4 {
			font-size: 1rem;
			color: var(--secondary-color);
			font-weight: bold;
			margin: 20px 0px;
		}
	}

	.skill-grid {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(6rem, 1fr));
		gap: 1rem;
	}

	.aboutme {
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

		.aboutme,
		.skills {
			flex: 1 1 0;
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
