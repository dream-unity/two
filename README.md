# Dream University

Repository: [dream-unity/two](https://github.com/dream-unity/two)  
Intended address: https://dreamuniversity.one/

Dream University’s world-creation university website, retaining the original Dream portal identity, parchment and ink palette, Palatino typography and architectural linework.

The academic experience includes four proposed schools, a five-stage Imagination & World Creation curriculum, three illustrative studio briefs, research directions and preparation guidance. The Dream Unity → Dream University → Dream Universe progression remains connected. The curriculum and schools are founding design proposals; the site does not represent enrolment or formal qualifications as available.

Native disclosures work without JavaScript. The small `university.js` enhancement opens a linked curriculum field or studio brief before scrolling, including direct fragment entry and back/forward navigation. The layout includes mobile breakpoints, reduced-motion preferences, a skip link, accessible artwork descriptions and visible keyboard focus.

## Artwork

`assets/worldbuilding-plate.webp` is a new illustration generated with the built-in image-generation tool, then encoded as WebP without visual alteration. The original portal asset is retained in the masthead and closing section. Studio illustrations and the favicon are code-native SVG.

Generation brief: a sophisticated Renaissance architect’s worldbuilding study on pale ivory parchment; a spherical miniature world with a terraced university city, domed observatory, delicate bridges, winding river, mountains and trees; exposed geology and roots beneath; fine compass construction lines and small unlabelled studies around it; warm monochrome ink and graphite, centered with clear paper margins, no text or modern UI.

## Checks

- JavaScript syntax checked with `node --check university.js`.
- Local asset paths, fragment links, unique IDs, image alternatives and accessible label references checked against the HTML.
- The custom-domain file and Pages publication marker are preserved.
- Browser rendering was not verified in the editing session because the supported preview capability was unavailable.

| Stage | Repository | Domain |
| --- | --- | --- |
| Dream Unity | `dream-unity/one` | `dreamunity.one` |
| Dream University | `dream-unity/two` | `dreamuniversity.one` |
| Dream Universe | `dream-unity/three` | `dreamuniverse.one` |

## Preparation and activation

`index.html`, `styles.css`, `university.js` and the artwork in `assets/` form a static site with no external runtime dependencies. `CNAME` contains only `dreamuniversity.one`; `.nojekyll` allows direct static publication. No install or build command is needed.

**Preparation is not activation.** Repository files do not establish that Pages settings, DNS or HTTPS are ready. This preparation has not changed those settings.

1. In [account Pages settings](https://github.com/settings/pages), verify ownership using GitHub's generated TXT challenge for this domain. Keep that record after verification.
2. Open [this repository's Pages settings](https://github.com/dream-unity/two/settings/pages). Choose **Deploy from a branch**, **main**, **/(root)** and save. Set **Custom domain** to **dreamuniversity.one** and save it before changing web-routing DNS.
3. In Namecheap, open **Domain List → Manage → Advanced DNS** for **dreamuniversity.one**. Replace the parking/redirect entries for `@` and `www` with the records below, using Automatic TTL. Preserve unrelated records and existing nameservers.

| Type | Host | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `dream-unity.github.io` |

The `www` target is the account hostname, without `/two`. Keep the existing IPv4-only configuration, matching Dream Unity.

4. Confirm the Pages deployment succeeds and the domain DNS check passes. Enable **Enforce HTTPS** when the certificate is ready; issuance and DNS propagation can take up to 24 hours.
5. Check HTTP and HTTPS for both apex and `www`: each must reach `https://dreamuniversity.one/` with the Dream University page and a valid certificate. Check all three navigation destinations after both new sites are activated.

Before activation, public DNS on 9 October 2026 showed `@` → `162.255.119.77` and `www` → `parkingpage.namecheap.com`. Inspect the current Namecheap zone before editing; public DNS does not expose Namecheap's internal redirect-rule type.

## Official setup references

- [GitHub publication source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [GitHub custom domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)
- [GitHub ownership verification](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages)
- [Namecheap GitHub Pages setup](https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages/)
