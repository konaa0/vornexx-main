<script>
	import Social from '../atoms/Social.svelte';
	import { user } from '../../util/discord';

	import { GitHubIcon } from '@indaco/svelte-iconoir/github';
	import { DiscordIcon } from '@indaco/svelte-iconoir/discord';
	import { MailIcon } from '@indaco/svelte-iconoir/mail';
	import { CubeHoleIcon } from '@indaco/svelte-iconoir/cube-hole';
	import { XIcon } from '@indaco/svelte-iconoir/x';
	import { SpotifyIcon } from '@indaco/svelte-iconoir/spotify';
	import { InstagramIcon } from '@indaco/svelte-iconoir/instagram';
</script>

<div class="socials-container">
	<Social tip="vornex-gh" link="https://github.com/vornex-gh">
		<GitHubIcon color="var(--accent)" />
	</Social>

	<Social tip={user.username} link={`https://discord.com/users/${user.id}`}>
		<DiscordIcon color="var(--accent)" />
	</Social>

	<Social tip="roblox profile" link="https://www.roblox.com/users/1016710675">
		<CubeHoleIcon color="var(--accent)" />
	</Social>

	<Social tip="spotify profile" link="https://open.spotify.com/user/bj9xmj4pmlqa86zym011zb1eb">
		<SpotifyIcon color="var(--accent)" />
	</Social>

	<Social tip="twitter/x profile" link="https://twitter.com/vornexx_">
		<XIcon color="var(--accent)" />
	</Social>

	<Social tip="instagram profile" link="https://instagram.com/vornexig">
		<InstagramIcon color="var(--accent)" />
	</Social>

	<Social tip="ajay.ramnath@courvix.com" link="mailto:ajay.ramnath@courvix.com">
		<MailIcon color="var(--accent)" />
	</Social>

</div>

<style>
	.socials-container {
		display: flex;
		gap: 0.75rem;
	}
</style>