# Druglord+ Website

Public privacy policy for Druglord+, developed by Ruan Vermeulen. Contact: contact@emberfallpress.com.

## Deploy to Cloudflare Pages

1. In your Cloudflare account, open Workers & Pages and create a Pages project by importing an existing Git repository.
2. Connect GitHub and select RuanVermeulen/DruglordPlus-Website.
3. Use these settings:

| Setting | Value |
| --- | --- |
| Project name | druglordplus-website |
| Production branch | main |
| Framework preset | None |
| Build command | exit 0 |
| Build output directory | public |
| Root directory | Leave blank |

4. Deploy and check the generated pages.dev URL.
5. In the Pages project, open Custom domains and add druglord.emberfallpress.com. Follow Cloudflare's activation flow and allow it to create the DNS record when offered.
6. If previously added, remove the old druglord CNAME pointing to custom-domains.chatgpt.site and the old _openai-site-verification.druglord and _cf-custom-hostname.druglord TXT records. Preserve unrelated website and email records.
7. Wait for the hostname and HTTPS certificate to become active. Verify the page opens publicly before using https://druglord.emberfallpress.com in Play Console.
8. Update the game's PrivacyPolicyUri and PRIVACY.md to the verified address and publish a new Android bundle.

Cloudflare hosts this static page in your account. Changes pushed to main deploy automatically after Git integration is enabled. The public folder contains all deployable content; no runtime dependencies or OpenAI hosting configuration are needed.

## Editing

Edit public/index.html to update the policy. Update its effective date when data practices change. Keep the Google Play Data safety form consistent with the shipped game and its third-party libraries.

Cloudflare documentation:
- https://developers.cloudflare.com/pages/framework-guides/deploy-anything/
- https://developers.cloudflare.com/pages/configuration/custom-domains/
