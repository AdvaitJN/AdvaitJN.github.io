<div class="social-bar">
	<span class="follow-text">FOLLOW ME</span>
	<div class="vertical-line"></div>
	<a
		href="https://www.linkedin.com/in/advaitjn/"
		class="icon-link"
		target="_blank"
		aria-label="LinkedIn"
	>
		<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32">
			<path
				d="M42,42H35.425V30.8c0-3.07-1.167-4.786-3.6-4.786-2.644,0-4.025,1.786-4.025,4.786V42H21.467V20.667H27.8V23.54a7.443,7.443,0,0,1,6.432-3.525c4.525,0,7.765,2.763,7.765,8.478ZM13.907,17.873a3.937,3.937,0,1,1,3.906-3.937A3.922,3.922,0,0,1,13.907,17.873ZM10.635,42h6.607V20.667H10.635Z"
				transform="translate(-10 -10)"
				fill-rule="evenodd"
			/>
		</svg>
	</a>
	<a href="https://github.com/AdvaitJN" class="icon-link" target="_blank" aria-label="Github">
		<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32.542 32">
			<path
				d="M16.285,0a16.422,16.422,0,0,0-5.15,31.969c.809.163,1.105-.353,1.105-.787,0-.38-.027-1.684-.027-3.042-4.53.978-5.473-1.956-5.473-1.956a4.191,4.191,0,0,0-1.807-2.39c-1.483-1,.108-1,.108-1a3.415,3.415,0,0,1,2.508,1.684,3.449,3.449,0,0,0,4.745,1.358,3.5,3.5,0,0,1,1.025-2.2C9.706,23.25,5.9,21.838,5.9,15.536a6.423,6.423,0,0,1,1.671-4.4A5.967,5.967,0,0,1,7.738,6.79s1.375-.435,4.475,1.684a15.524,15.524,0,0,1,8.142,0c3.1-2.119,4.476-1.684,4.476-1.684a5.966,5.966,0,0,1,.162,4.346,6.3,6.3,0,0,1,1.672,4.4c0,6.3-3.8,7.687-7.441,8.094a3.9,3.9,0,0,1,1.105,3.042c0,2.2-.027,3.966-.027,4.509,0,.435.3.951,1.105.788A16.422,16.422,0,0,0,16.285,0Z"
				fill-rule="evenodd"
			/>
		</svg>
	</a>
</div>

<style lang="scss">
	/* Base styles (applied to all devices) */
	.social-bar {
		position: absolute;
		top: 20%;
		right: 60px;
		display: flex;
		flex-direction: column;
		align-items: center;
		z-index: 1000;

		.follow-text {
			color: var(--primary-color);
			font-size: 1rem;
			writing-mode: vertical-rl;
		}

		.vertical-line {
			width: 2px;
			height: 200px;
			background-color: var(--primary-color);
			margin: 37.5px 0;
		}

		.icon-link {
			margin: 10px 0;
			svg {
				width: 32px;
				height: 32px;
				fill: var(--primary-color);

				&:hover {
					fill: var(--secondary-color);
				}
			}
		}
	}

	/* Large screens (≥992px) */
	@media (min-width: 992px) {
		.social-bar {
			position: fixed;
		}
	}
</style>
