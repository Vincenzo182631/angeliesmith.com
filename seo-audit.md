# SEO Audit — angeliesmith.com

Nov 16, 2026

angeliesmith.com has a clean crawl base but needs work: no product page carries Product schema, the blog has been idle since March 2025, and duplicate archives dilute a small 81-URL site.

## Executive summary

**Overall: needs work.** The foundation is sound, but the store is invisible to rich results and its content has stalled.

**Biggest strength:** crawl hygiene. All 81 sitemap URLs resolve over HTTPS with self-referencing canonicals, single-hop redirects, and unique titles and descriptions on every product page. The site also holds a real niche (Procell microchanneling) where competitors are weak.

**Top 3 priorities:**

1. **Add Product schema to the 29 live product pages.** None outputs Product, Offer or rating markup, so Google cannot show price, stock or stars, and the products are not eligible for free merchant listings.
2. **Remove duplicate and broken URLs.** Nine tag archives and four brand archives duplicate the product categories, one sitemap product URL redirects to a PNG image, and blog posts contain three internal 404s plus old Shopify links.
3. **Restart content around microchanneling.** The blog has five posts, the newest from 1 March 2025, with no Article schema and the author shown as "mrgreat". The homepage H1 still reads "Best Skin Care Products of 2025".

Ahrefs Domain Rating is 31. Ranking, traffic and search-volume figures are not in this audit because the connected Semrush, Ahrefs and SEO Gets accounts had no usable quota (see Method and limits).

## Prioritized action plan

### Quick wins (this week)

| # | Action | Impact | Effort | Depends on |
| --- | --- | --- | --- | --- |
| 1 | Enable Product structured data (WooCommerce's built-in output is missing; check the theme or an optimisation plugin stripping it, or turn on Yoast WooCommerce SEO). Validate in Google's Rich Results Test. | High | 1–2 h | WP admin access |
| 2 | Fix `/maree-hair-serum/`: it 301s to a PNG file. Restore the product page or remove it from the catalogue and its 15 internal links. | High | 30 min | — |
| 3 | Set product tag archives to noindex in Yoast (Search Appearance → Taxonomies). Pick brand archives or product categories as the indexable set and noindex or redirect the other. | High | 30 min | Decision on brand vs category URLs |
| 4 | Fix blog links: 3 internal 404s, the dead angeliesmithbeauty.com link, and old `/products/` and `/collections/` Shopify URLs in 3 posts. | Medium | 1 h | — |
| 5 | Rewrite the homepage H1 (drop "2025") and add alt text to the 30 homepage images without it. | Medium | 1 h | — |
| 6 | Set Yoast Site Representation to Organization or Person with logo and social profiles, so Organization schema is output. Rename author "mrgreat" to Angelie Smith with a nurse bio. | Medium | 30 min | — |
| 7 | Add titles and descriptions to `/prolon-fasting-next-gen/`, `/policies/*` and `/category/blog-posts/`. Add an H1 to `/faq/` and change the blog H1 from "Blogs". | Medium | 1 h | — |
| 8 | Fix typos in indexed copy: "Microchanelling", "Ultra-RichNight", "MimickingDiet", "for trusted trust"; align `/skin-brightening-system/` title (Normal to Dry) with its H1 (Normal to Oily). | Low | 30 min | — |
| 9 | Add `rel="sponsored nofollow"` to the 19 of 32 affiliate and partner links that lack it (Amazon, Awin, Prolon, L-Nutra). | Medium | 30 min | — |
| 10 | Compress the three homepage PNGs of 0.8–1.6 MB each to WebP under 150 KB. | Medium | 30 min | — |

### Strategic investments (this quarter)

| # | Action | Impact | Effort | Depends on |
| --- | --- | --- | --- | --- |
| 1 | Build a microchanneling topic cluster: one pillar guide plus 8–10 supporting posts (see Content gaps), each linking to the matching Procell product. | High | Multi-week, 2 posts a month | Author bio and Article schema live |
| 2 | Turn on full-page caching at Hostinger CDN (pages are served `no-store` and uncached today) and load Stripe, PayPal and hCaptcha only at checkout. | High | 1–2 days | Developer or host support |
| 3 | Rewrite product copy with first-hand nurse commentary, usage photos and FAQs. Collect reviews: products show 0–1 reviews. | High | Multi-week | Product schema live |
| 4 | Strengthen trust signals for health content: link license and certifications from every post, cite sources, add FAQPage markup to `/faq/`. | Medium | 2–3 days | — |
| 5 | Earn links through the professional angle: Procell provider directories, esthetician and nursing publications, guest features. | Medium | Ongoing | Cluster content published |
| 6 | Clarify the brand. The site calls itself "Beauty Health", a generic name also used by a large listed skincare company, while the domain and all trust content say Angelie Smith. | Medium | Half day | Owner decision |
| 7 | Connect Search Console data (upgrade the site in SEO Gets or add Semrush or Ahrefs units) so rankings and volumes can be measured. | Medium | 1 h | Account upgrade |

## On-page issues

Sorted by severity. Every one of the 81 sitemap URLs was fetched and parsed.

| Page | Issue | Severity | Recommended fix |
| --- | --- | --- | --- |
| All 29 live product pages (25 sold on-site, 4 Maree affiliate listings) | No Product, Offer or AggregateRating schema; only WebPage and Breadcrumb are output | Critical | Restore WooCommerce Product JSON-LD with price, availability, brand, GTIN and reviews |
| `/maree-hair-serum/` | Listed as a product in the sitemap but 301s to `/wp-content/uploads/2026/01/maree-hair-serum.png`; 15 pages link to it | Critical | Rebuild the product page or remove the product and its links |
| 9 `/product-tag/*` archives | Indexable, default "Archives" titles, no descriptions; `/product-tag/procell/` and `/product-tag/procell-therapies/` are identical | High | Noindex all product tags; merge the two Procell tags |
| `/brand/*` vs `/product-category/*` | Four brand archives list the same products as the Obagi, Procell, Prolon and Maree categories and compete for the same keywords | High | Keep one set indexable; 301 or canonicalise the other |
| Homepage | H1 is "Best Skin Care Products of 2025"; 37 H2s, most of them product names; 30 of 69 images lack alt text | High | New H1 matching the title's intent; demote product names to H3; add alt text |
| 5 blog posts | No Article schema; author is "mrgreat"; newest post dated 1 Mar 2025 | High | Rename author, add a nurse bio and credentials, enable Article schema, refresh the posts |
| `/best-serum-microchanneling/`, `/microchanneling-basics/` | Links to 3 internal 404s and the dead domain angeliesmithbeauty.com | High | Point the links at the live product URLs |
| 3 blog posts, `/prolon-fasting-next-gen/` | Old Shopify `/products/` and `/collections/` links (redirecting) and images hotlinked from cdn.shopify.com | Medium | Update links; upload the images to WordPress before the old store's CDN drops them |
| `/prolon-fasting-next-gen/` | Linked from all 80 pages, yet has a default title, no description and overlaps the `/next-gen-prolon/` product | Medium | Write title and description; differentiate it as a guide or merge into the product |
| `/microchanneling-device/` | 67 words on a page targeting a commercial B2B query; linked sitewide | Medium | Expand to 600+ words: specs, training, pricing path, FAQ |
| `/obagi-vitamin-c/`, `/procell-therapies/`, `/md-aftercare/` | URL does not match the product: Microdermabrasion Polish + Mask, PRO Facial Serum and MD Step 2 respectively | Medium | Rename slugs with 301s, e.g. `/obagi-professional-c-polish-mask/`, `/procell-pro-facial-serum/`, `/procell-md-aftercare-step-2/` |
| `/skin-brightening-system/` | Title says "Normal to Dry", H1 says "Normal to Oily" | Medium | Make both match the product sold |
| `/faq/` | No H1 and no FAQPage schema on 671 words of Q&A | Medium | Add an H1 and FAQPage markup |
| `/blog/`, `/category/blog-posts/` | H1 is "Blogs" with 52 words; the category archive has no H1 or description and no inbound links | Medium | Rename the H1, add an intro; noindex the single category archive |
| Affiliate links sitewide | 19 of 32 affiliate or partner links lack `rel="sponsored"` or `nofollow` | Medium | Add the attribute and a visible disclosure near the links |
| `/policies/*` (4 pages) | Default titles, no meta descriptions | Low | Add descriptions or leave; low search value |
| `/about/`, `/certifications/`, `/contact/` | 57–172 words each; certification images have no alt text | Low | Expand the About page with credentials and experience; add alt text |
| Several titles and H1s | Typos: "Microchanelling", "Ultra-RichNight", "MimickingDiet", "for trusted trust" | Low | Correct the spelling |
| Social tags | `og:image` is the 812×277 logo on the homepage; `og:title` differs from the title tag | Low | Use a 1200×630 share image |

## Technical SEO checklist

Speed figures are lab measurements from one headless Chromium run emulating a Pixel 7 on a fast connection, not Google field data. Real phones on mobile networks will be slower.

| Check | Status | Details |
| --- | --- | --- |
| HTTPS and redirects | Pass | HTTP and www both 301 to `https://angeliesmith.com/` in one hop; no mixed content; CSP upgrades insecure requests. No HSTS header. |
| robots.txt | Pass | Blocks only WooCommerce logs, uploads, add-to-cart and wp-admin; references the sitemap index |
| XML sitemap | Warning | Yoast index with 7 child sitemaps, 81 URLs. Includes noindexed `/cart/`, `/checkout/`, `/my-account/` and the `/maree-hair-serum/` redirect. No page lastmod is newer than 13 Jan 2026. |
| Canonical tags | Pass | Self-referencing on every indexable page |
| Indexation and duplicates | Fail | 13 thin tag and brand archives duplicate category pages; index coverage itself could not be verified without Search Console |
| Structured data | Fail | WebPage, WebSite and Breadcrumb only. Missing Product, Organization, Article and FAQPage. |
| Broken links | Warning | 3 internal 404s, 1 dead external domain, 1 product URL redirecting to an image; missing URLs correctly return 404 |
| Mobile-friendliness | Pass | Viewport set, no horizontal scroll at 412 px; 28 links or buttons on the homepage are under 24 px in one dimension |
| Server response and caching | Warning | Homepage first byte 0.8–1.5 s; other pages 0.2–0.8 s. Responses are `no-store` and CDN status is DYNAMIC, so HTML is never cached. |
| LCP (lab) | Warning | Homepage 3.9 s, product page 3.4 s, blog post 0.9 s. Google's "good" threshold is 2.5 s. |
| CLS (lab) | Pass | 0 on all three templates |
| Page weight | Fail | Product page: 267 requests and about 23 MB of uncompressed JavaScript, driven by Stripe, PayPal and hCaptcha loading on every product view. Homepage: 117 requests, 3.4 MB of JavaScript. |
| Images | Warning | Homepage serves three PNGs of 1.6 MB, 1.4 MB and 0.8 MB; the LCP image is a JPEG uploaded from WhatsApp; 28 of 69 homepage images are not lazy-loaded |
| Third-party scripts | Warning | Omnisend, Pinterest, Google Ads, Tag Manager, Sentry and CodeDrink load on every page |

## Keyword opportunities

Microchanneling and Procell terms are the best opening: the results are held by small clinic sites and low-authority resellers, while Obagi and Prolon head terms are held by brand sites with Domain Rating 70+. Difficulty and opportunity are estimates from who ranks today, not measured volumes; current rankings are unknown without Search Console or a paid rank tool.

| Keyword | Est. difficulty | Opportunity | Intent | Target page or content type |
| --- | --- | --- | --- | --- |
| procell md aftercare serum | Easy | High | Transactional | Product: `/procell-md-aftercare/` |
| procell microchanneling aftercare | Easy | High | Informational | New guide linking to Step 1 and Step 2 |
| what to put on skin after microchanneling | Easy | High | Informational | New post |
| procell pro vs md serum | Easy | High | Commercial | Refresh `/best-serum-microchanneling/` |
| microchanneling vs microneedling | Moderate | High | Informational | Refresh `/microchanneling-or-microneedling/` |
| what is microchanneling | Moderate | High | Informational | Pillar: rebuild `/microchanneling-basics/` |
| how often should you do microchanneling | Easy | High | Informational | New post |
| microchanneling for hair loss | Moderate | High | Informational | New post linking to `/procell-hair-aftercare/` |
| procell microchanneling device for estheticians | Easy | High | Commercial (B2B) | Expand `/microchanneling-device/` |
| how to use procell serum at home | Easy | High | Informational | Refresh `/how-to-use-procell-serums/` |
| microchanneling before and after | Moderate | Medium | Informational | New post with dated result photos |
| microchanneling cost | Moderate | Medium | Informational | New post |
| obagi nu-derm fx how to use (order of steps) | Moderate | Medium | Informational | New guide linking to the system kit |
| obagi nu-derm normal to dry vs normal to oily | Easy | Medium | Commercial | Comparison post |
| obagi professional-c 10 vs 15 vs 20 | Moderate | Medium | Commercial | Comparison post |
| obagi elastiderm eye cream review | Moderate | Medium | Commercial | First-hand review on the product page |
| prolon 5 day fast what to expect day by day | Moderate | Medium | Informational | New guide |
| prolon next gen vs original | Easy | Medium | Commercial | Convert `/prolon-fasting-next-gen/` |
| prolon reset 5:2 review | Easy | Medium | Commercial | Review on `/reset-bundle/` |
| fasting mimicking diet for skin | Easy | Medium | Informational | New post bridging the two niches |
| obagi vitamin c serum | Hard | Low | Transactional | Product: `/vitamin-c/` |
| fasting mimicking diet | Hard | Low | Informational | Covered by the Prolon guide |

## Content gaps

The site sells three product lines but publishes on one: all five posts cover microchanneling, and nothing supports the 13 Obagi or 7 Prolon products.

| Topic | Why it matters | Format | Priority | Effort |
| --- | --- | --- | --- | --- |
| Microchanneling aftercare: day-by-day routine | Clinic sites rank with short pages; the site sells the exact aftercare products | Guide | High | Moderate (half day) |
| Microchanneling pillar: what it is, benefits, risks, who it suits | Anchors the cluster; existing post is 756 words from July 2024 | Pillar page | High | Substantial |
| Refresh the 5 existing posts | 20–28 months old, broken links, no author credentials | Update | High | Quick win each (1–2 h) |
| Microchanneling for hair regrowth | A hair-clinic site ranks for the comparison query; the site sells Procell Hair Aftercare | Blog post | High | Moderate |
| Microchanneling device buyer page for professionals | Decision-stage B2B page is 67 words | Landing page | High | Moderate |
| Obagi Nu-Derm routine: step order, AM and PM, what to expect | No consideration-stage content for the largest product line | Guide | Medium | Moderate |
| Obagi comparisons: Nu-Derm skin types, Professional-C strengths | Decision-stage queries with clear buying intent | Comparison pages | Medium | Moderate each |
| Prolon 5-day fast: day-by-day experience from a nurse | First-hand experience is the edge over the brand site | Guide | Medium | Moderate |
| Prolon Next Gen vs original, Reset 5:2 explained | Product launches with little independent coverage | Comparison page | Medium | Quick win |
| Product FAQs and reviews on each product page | Products show 0–1 reviews; FAQ content can earn rich results once marked up | On-page blocks | Medium | Substantial across the catalogue |
| Video transcripts on `/videos/` | 138 words; videos carry no indexable text or VideoObject schema | Page upgrade | Low | Moderate |
| `/resources/` business tools page | Off-topic affiliate links (Canva, Fiverr, Envato) on a skincare site; 172 words | Noindex or move | Low | Quick win |

Funnel view: awareness has 5 dated posts, consideration has none (no comparisons or reviews), and decision pages exist but lack schema, reviews and first-hand copy.

## Competitor comparison

At Domain Rating 31, the site matches the content peers that rank for microchanneling queries and is far behind the brand sites, which is why the plan targets Procell and microchanneling first. No competitors were supplied, so these were taken from live search results for the target queries on 16 Nov 2026.

| Domain | Role | Domain Rating (Ahrefs) | Seen ranking for |
| --- | --- | --- | --- |
| angeliesmith.com | This site | 31 | Not seen in the sampled results |
| [azulbeauty.com](https://azulbeauty.com/have-you-heard-of-microchanneling-its-even-better-than-microneedling/) | Med-spa blog, content peer | 33 | microchanneling vs microneedling; products to combine with microchanneling |
| [browandbeautybar.com](https://browandbeautybar.com/blog/how-to-take-care-of-your-skin-after-procell-microchanneling-therapy) | Clinic blog, content peer | 30 | Procell aftercare |
| [medpurchasing.com](https://medpurchasing.com/product/md-aftercare-step-2-healing-accelerator/) | Procell reseller, retail peer | 5 | Procell MD aftercare product queries |
| [jaepakmd.com](https://jaepakmd.com/resources/microchanneling-vs-microneedling-whats-better-for-hair-loss/) | Hair clinic | Not checked | microchanneling vs microneedling for hair loss |
| procelltherapies.com | Brand site | 74 | Procell brand terms |
| obagi.com | Brand site | 74 | Obagi product terms |
| prolonlife.com | Brand site | 70 | Prolon and fasting mimicking diet terms |
| dermstore.com | Large retailer | 78 | Obagi product terms |

| Dimension | angeliesmith.com | Content peers (DR 30–33) | Winner |
| --- | --- | --- | --- |
| Authority | DR 31 | DR 30–33 | Even |
| Publishing | 5 posts, none since Mar 2025 | Ranking with single clinic posts | Open |
| Commercial fit | Sells the Procell aftercare and serums the queries are about | Clinics selling treatments, not products | angeliesmith.com |
| Author credentials | Licensed nurse, certifications page, but not shown on posts | Clinic practitioners | Peers, until bios are added |
| Rich results | No Product, Article or FAQ schema | Not audited | Unknown |

A reseller with Domain Rating 5 appears for Procell product queries, so these terms are winnable with correct product markup and stronger pages. Keyword counts, backlink profiles and SERP-feature ownership need a paid Ahrefs or Semrush plan.

## Method and limits

- **Crawled:** all 81 URLs in the Yoast sitemap index on 16 Nov 2026, plus status checks on 337 internal and external links found in them.
- **Measured:** titles, descriptions, headings, canonicals, robots tags, JSON-LD types, word counts, image alt text and internal links per page; load metrics from one headless Chromium run per template.
- **Authority:** Ahrefs free Domain Rating lookup.
- **Not available:** Semrush (no API units left), Ahrefs Site and Keywords Explorer (free plan), SEO Gets (site is on the free tier, so no Search Console data), Google PageSpeed Insights (shared quota exhausted). Rankings, traffic, search volumes, backlink detail and Core Web Vitals field data are therefore missing.
- **Not checked:** Google index coverage, manual actions, and competitor on-page quality.
- **Platform:** WordPress with WooCommerce and Yoast SEO, PHP 8.2, served through Hostinger's CDN. Fixes are made in WordPress admin.
