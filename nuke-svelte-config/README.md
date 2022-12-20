# Houdini version
- houdini: 0.18.3
- houdini-svelte: 0.18.3

# The issue
`npx houdini init` ignores the existing `svelte.config.js` file, and replaces it with its own minimal version, with the houdini alias added.

Tested on: Windows 11

# Reproduce
1. Open the `svelte.config.js` file, and take note of the `prerender` option in there.
2. `npm install`
3. `npx houdini init`

-> you'll see that the svelte.config.js has been changed, and the existing options have been thrown away.

Additionally, it creates the `vite.config.ts` file, even though there already is a `vite.config.js`
