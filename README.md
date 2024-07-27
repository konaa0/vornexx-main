## ☁️ Hosting

Steps to follow if you want to replicate the hosting of this site. You may host with whatever service you prefer.

1. Go to [Cloudflare Pages](https://pages.dev/)
2. Create a project and connect your repository
3. Under `Build settings`, select the `SvelteKit` preset
4. Under `Environmental variables (advanced)`, add the following variable:
   - Variable name: `NODE_VERSION`
   - Value: `21`
5. Save and deploy

All website-related code is distributed under the [AGPL license](LICENSE).
