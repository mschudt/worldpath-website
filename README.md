# Worldpath website

Public website and bilingual privacy policy for Worldpath.

## Files

- `index.html`: app information and support contact.
- `privacy/index.html`: English and German privacy policy.
- `.nojekyll`: serves the site as static HTML without a Jekyll build.

## Publish

From this directory:

```sh
git add .
git commit -m "Publish Worldpath website and privacy policy"
git push -u origin main
```

Then open the repository on GitHub and choose **Settings → Pages**:

1. Source: **Deploy from a branch**.
2. Branch: **main**.
3. Folder: **/ (root)**.
4. Click **Save** and wait for the Pages deployment to finish.

Expected URLs after deployment:

- Website: https://mschudt.github.io/worldpath-website/
- Privacy: https://mschudt.github.io/worldpath-website/privacy/

Check both URLs without signing in. Put the privacy URL in Google Play Console
under App content → Privacy policy, and use the website URL in the store's
website field. The app currently displays its policy text internally and does
not hardcode the old Worldpath website URL, so this hosting change alone does
not require an app rebuild. The old `worldpath-app` URL will not automatically
redirect to the new site.

For future policy changes, edit `privacy/index.html`, commit, and push to `main`.

## Source

The initial HTML files were copied from `docs/` in the private Worldpath app
repository. That source directory was retained because the app's release tests
currently reference it. No app source, signing material, or travel data belongs
in this public repository.
