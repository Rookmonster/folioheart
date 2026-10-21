# Folioheart — GitHub Pages upload files

This folder is already built. No npm, Node, or Actions workflow is required.

## Upload and publish

1. Create or open a GitHub repository named **folioheart**.
2. Unzip `Folioheart-github-pages.zip` on your computer. Upload its **extracted files** to the repository's top level. `index.html` and `manifest.json` must be at the top level, not inside a folder or left inside the ZIP.
3. Make sure the empty `.nojekyll` file is included. If your computer hides it, use GitHub's **Add file → Create new file**, name it `.nojekyll`, and commit it.
4. In the repository, go to **Settings → Pages**. Under Source, select **Deploy from a branch**. Select **main**, choose **/(root)**, and save. See [GitHub's instructions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).
5. Wait for GitHub Pages to finish deployment. Its site URL is shown on the Pages settings screen. Open it and verify the app loads.
6. Add `manifest.json` to that published URL and use it as your Owlbear extension installation link. For a standard project repository, this is:

   `https://YOUR-USERNAME.github.io/folioheart/manifest.json`

7. In Owlbear Rodeo, open your profile's **Extensions**, choose **Add Extension**, paste the manifest URL, and enable Folioheart in your campaign room. Each player then opens the extension from the room.

Do not use a `github.com/.../blob/...` link or a `raw.githubusercontent.com` link as the installation URL. Use the published `github.io` site.

## Update an existing installation

Replace the extracted files in the existing repository, commit them, and wait for the GitHub Pages deployment to succeed. Reopen Folioheart in Owlbear Rodeo to load the new version. Existing characters are preserved. Your installation link remains the same.

## Repository name and paths

The manifest is configured for `/folioheart/`. Owlbear resolves extension paths from the site's origin, so GitHub Pages project sites need their repository prefix. If you use another project repository name, change all three asset paths in `manifest.json` to include that name. The page's own stylesheet, JavaScript and images use relative paths.

For a user-site repository named `YOUR-USERNAME.github.io`, use `/icon.svg` for both icon fields and `/index.html` for the popover; the install link is `https://YOUR-USERNAME.github.io/manifest.json`. For a custom domain, adjust the manifest prefix to match the actual deployed folder.

## Included behavior

- Individual class/domain selections with player-controlled selection locks.
- 189 domain, 18 ancestry and 9 community core cards, plus class/subclass references.
- GM-managed communal party cards; players can view them.
- Custom ancestry and domain cards.
- Mixed / hybrid ancestry in Character details: first trait of one ancestry plus second trait of another, shown together with resource trackers.
- Delete your own saved character with typed confirmation; retain your custom library by default or delete it too.
- Card-local resource counters, effect dice, limited uses, rolled Prayer Dice, and configurable custom trackers. Resources remain usable while card selections are locked.
- Separate personal/party persistence and JSON backups containing tracker state.

This bundle contains no saved campaign, character or player data. The published site does not need a database or account keys. Owlbear room metadata stores campaign state. Locks and role checks are app-level controls, not a separate security backend.

This update was checked using a simulated Owlbear SDK host. Run an in-room check after publishing.

See `DPCGL.pdf` and the in-app Credits for game-content attribution and terms. This build was prepared as a private campaign companion; hosting access and public redistribution remain subject to those terms. SDK licensing is included in `SDK-LICENSE.txt`.
