# The Express Massage website

Static GitHub Pages site for The Express Massage, a Jakarta 24-hour mobile massage service.

## Files

- `index.html` - landing page, SEO metadata, schema.org business data
- `assets/styles.css` - responsive visual design
- `assets/app.js` - Indonesian, Japanese, and English language switching
- `assets/hero-genspark-gpt-image-2.png` - current hero image. For future replacements, generate through the project Genspark CDP image-generation guide, not the Genspark Super Agent chat.

## Image generation workflow

Use the guide at:

`C:\Users\denty\Project\.o11y\genspark-inapp-api\CLAUDE-SESSION-GUIDE.md`

Correct workflow:

1. Confirm Chrome CDP on `http://127.0.0.1:9223/json/version`.
2. Open Genspark image agent: `https://www.genspark.ai/agents?type=image_generation_agent&action=chat_now`.
3. Use `generateGptImage2ViaCdp()` from `api-spec/genspark-cdp-bridge.mjs`.
4. Set `aspectRatio: "16:9"` for the site hero and `waitForResult: true`.
5. Save the result with `saveBestMediaCandidate()` into this repo's `assets` directory.

Do not use the Super Agent route for image assets because it consumes unnecessary credits and does not follow the project CDP workflow.

## GitHub Pages

Publish from the repository root on the `main` branch. When the custom domain is ready, add the domain in GitHub Pages settings and create a `CNAME` file containing the domain.
