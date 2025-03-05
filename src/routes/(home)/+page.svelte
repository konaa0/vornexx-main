<script lang="ts">
	import Clock from './Clock.svelte';
	import DiscordInfo from './DiscordInfo.svelte';
	import SocialLink from './SocialLink.svelte';
	import SpotifyInfo from './SpotifyInfo.svelte';

	import Discord from '$lib/components/icons/Discord.svelte';
	import GitHub from '$lib/components/icons/GitHub.svelte';
	import Envelope from '$lib/components/icons/Envelope.svelte';
	import Spotify from '$lib/components/icons/Spotify.svelte';
	import Meta from '$lib/components/Meta.svelte';
</script>

<Meta title="vornexx" description="My portfolio and personal website." />

<main class="wrapper fade">
	<h1 class="header">vornexx</h1>

	<p class="mt-4 text-gray-400">
		I'm <b>vornexx.</b>, a person from
		<b>Trinidad & Tobago (Trinidad)</b>.
		In my free time I play Genshin Impact or Roblox or watch shows or movies.
	</p>

	<div class="mt-4 flex gap-6">
		<SocialLink href="https://discord.com/users/1149438819834269856" name="Discord">
			<Discord />
		</SocialLink>

		
		<SocialLink href="https://github.com/vornexx" name="GitHub">
			<GitHub />
		</SocialLink>

	
		<SocialLink
			href="https://spotify.vornexx.is-a.dev"
			name="Spotify"
		>
			<Spotify />
		</SocialLink>

		<SocialLink href="mailto:vornexx@disroot.org" name="Email">
			<Envelope />
		</SocialLink>
	</div>

	<Clock />

	<DiscordInfo />
	<SpotifyInfo />
</main>
