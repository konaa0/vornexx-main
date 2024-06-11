<script>
	import RichPresence from '../molecules/RichPresence.svelte';
	import Tooltip from '../atoms/Tooltip.svelte';

	// i didnt write this idk
	let getAge = () => {
		let birthDate = new Date('2009/08/16');
		const ageMs = Date.now() - birthDate.getTime();
		const preciseAge = (ageMs / 31536000000).toFixed(10);
		return preciseAge;
	};

	let age = getAge();
	setInterval(() => {
		age = getAge();
	}, 1000);
</script>

<section id="about" class="wrapper">
	<div>
		<RichPresence />
	</div>
	<div class="text">
		<h2>bio</h2>
		<p>
			Hey there, I'm vornexx! I'm a <Tooltip tip={age}
				><span>{Math.floor(Number(age))}</span></Tooltip
			>
			year old that is learning tech as I go, I usually use HTML and CSS, but I'm always open to learn about anything, if you wanna check out my unorganized spotify playlist
			<Tooltip tip="🎵">
				<a href="https://spotify.vornexx.is-a.dev" target="_blank" rel="noreferrer">
					<span>click here</span>
				</a>
			</Tooltip>
			. I have an .mp4 dump site if you wanna check out that "archive"
			<Tooltip tip="📽️">
				<a href="https://cdnvnx.vercel.app" target="_blank" rel="noreferrer">
					<span>.mp4 dump site</span>
				</a>
			</Tooltip>
		    . Aside from this, I have a blog page you can view aswell
		    <Tooltip tip="✍️">
			<a href="https://blog.vornexx.is-a.dev" target="_blank" rel="noreferrer">
				<span>here</span>
			</a>
		    </Tooltip>	

		</p>
	</div>
</section>

<style lang="scss">
	@import '../../styles/mixins.scss';

	section {
		margin-bottom: 6rem;
		display: grid;
		gap: 4.5rem;
		grid-template-columns: 1fr 1fr;
		align-items: center;
	}

	.text {
		position: relative;
		line-height: 1.75rem;
	}

	span {
		font-weight: 400;
		font-family: var(--font-two);
		font-size: 0.9rem;
		background-color: var(--elevation-one);
		border-radius: 7px;
		color: var(--accent);
		padding: 0.2rem 0.5rem 0.2rem;
		width: fit-content;
	}

	a {
		text-decoration: none;
	}

	.text::before {
		@include outlineText(
			$content: 'vor',
			$translateX: 97%,
			$translateY: -5%,
			$fontSize: 300px,
			$opacity: 0.22
		);
	}

	h2 {
		display: none;
		margin-top: 1rem;
	}

	@media (max-width: 868px) {
		section {
			display: flex;
			flex-direction: column;
			align-items: normal;
		}

		h2 {
			display: block;
			margin-bottom: 1rem;
		}
	}
</style>
