# Squeaky — marketing website

Static landing page for the Squeaky iOS app, plus the **Privacy Policy** and
**Support** pages required for App Store submission.

```
index.html      landing page
privacy.html    privacy policy  (App Store "Privacy Policy URL")
support.html    support page    (App Store "Support URL")
styles.css      shared styles (brand: mint + blush pink + coral, Fredoka font)
assets/
  icon.png      app icon
  slides/       the 10 finished App Store screenshot slides
  hero.png      splash hero (spare)
```

Pure static HTML/CSS — no build step. Fonts load from Google Fonts.

## Preview locally
```bash
cd squeaky-clean-web
python3 -m http.server 8777
# open http://localhost:8777
```

## Deploy (GitHub Pages)
1. Create a repo and push these files.
2. Settings → Pages → deploy from `main`, root.
3. Your pages appear at `https://<username>.github.io/<repo>/`.
4. **Update the app's URLs to match** in `../squeekyclean/Squeaky/Support/Legal.swift`
   and `../squeekyclean/fastlane/metadata/en-US/{privacy,support,marketing}_url.txt`,
   then re-run `fastlane metadata`. (These currently point at the `sreejith.github.io`
   placeholder — set them to the real hosted URL.)
