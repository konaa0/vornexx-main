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
			Hey there, I'm vornexx! 💖 I'm a <Tooltip tip={age}
				><span>{Math.floor(Number(age))}</span></Tooltip
			>
			year old that is learning tech as I go, I usually use HTML and CSS, but I'm always open to learn about anything. Thanks to <span>afn.im</span> I learnt about <span>Svelte</span>. This website is also
			<Tooltip tip="💝">
				<a href="https://github.com/xafn/afn.im" target="_blank" rel="noreferrer">
					<span>open-source</span>
				</a>
			</Tooltip>
			, if you wanna check out my unorganized spotify playlist
			<Tooltip tip="🎵">
				<a href="https://spotify.vornexx.is-a.dev" target="_blank" rel="noreferrer">
					<span>click here</span>
				</a>
			</Tooltip>
		    , aside from this I use a 
			<Tooltip tip="💻">
				<a href="https://valid.x86.fr/y10l2a" target="_blank" rel="noreferrer">
					<span>Dell Inspiron 3583</span>
				</a>
			</Tooltip>
			as a main computer and I also use a 
			<Tooltip tip="📞">
				<a href="https://www.gsmarena.com/samsung_galaxy_a54-12070.php" target="_blank" rel="noreferrer">
					<span>Samsung Galaxy A54 5G</span>
				</a>
			</Tooltip>
			as a main phone that runs pretty well for a budget phone, basically a flagship from 2020/2021. If you care to watch, I shitpost monthly(strong maybe) on this
			<Tooltip tip="📽️">
				<a href="https://cdn-vornexx.vercel.app" target="_blank" rel="noreferrer">
					<span>.mp4 dump site</span>
				</a>
			</Tooltip>
		    . I have a Rentry .md page you can view
		    <Tooltip tip="✍️">
			<a href="https://rentry.co/vornexx" target="_blank" rel="noreferrer">
				<span>here</span>
			</a>
		    </Tooltip>
			And lastly I have a guestbook where you are free to type whatever you want, whenever you want whether it be anonymous or not
		    <Tooltip tip="📝">
			<a href="https://vornexx.123guestbook.com/" target="_blank" rel="noreferrer">
				<span>here</span>
			</a>
			</Tooltip>
			.
			

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
