# 15. Audit landing pages and websites for SEO/GEO

```text
Audit our landing pages and website for SEO and GEO (generative engine optimization: visibility and accurate representation in AI-powered search and answers).

Context, if known:
- Website and priority URLs: [domain, URLs, sitemap, or preview]
- Product and intended audience: [description]
- Markets and languages: [details]
- Main conversion: [signup, purchase, demo, contact, or other outcome]
- Priority searches and competitors: [optional]
- Available access: [repository, Search Console, Bing Webmaster Tools, analytics, or logs]

This is an audit. You may inspect public pages, available source code, and authorized analytics, run non-destructive checks, draft improvements in the report, and save audit artifacts. This overrides the shared implementation permissions: leave application files, CMS content, search settings, crawler policies, and live deployments unchanged until I request implementation.

Identify the pages the owner wants people to find through search and the pages they want excluded. Identify production versus preview environments. If you cannot identify the website or audience from the available context, ask for it and continue checks that do not depend on the answer.

Inspect every nominated priority URL. For larger sites, inventory relevant URLs and sample representative templates, languages, and page types; state the sample and coverage limits. Keep crawling within the stated site scope and avoid unbounded parameter combinations. Compare HTTP responses and initial HTML with browser-rendered content where tools permit. Distinguish repository findings from observed deployed behavior.

Use current official search-engine and provider documentation for technical rules, bot controls, structured-data eligibility, and measurements. Cite sources and the audit date. Label judgment calls and experiments, and cite provider evidence for claims about ranking factors.

Check these areas where applicable:

1. Discovery and technical eligibility
Inspect response codes, redirect chains, soft errors, robots.txt, robots meta tags, X-Robots-Tag, canonical URLs, sitemaps, internal links, and access restrictions. Check JavaScript rendering, crawlable navigation, duplicate URLs, and multilingual annotations. Check that visitors and the intended crawlers can access the content and follow its links. Distinguish crawling, indexing, and ranking. Use authoritative inspection data when available; absence from a search or site: query alone does not establish an indexing failure. Preserve deliberate exclusions for private, duplicate, or preview pages.

2. Page purpose and search intent
Determine what question or task each landing page should satisfy. Assess descriptive titles and meta descriptions, logical headings, useful internal links, image alternatives, URL clarity, content overlap, and intent alignment. Check whether visitors can understand the product, audience, value, limitations, and next step. Identify thin or redundant pages without assuming that a particular word count, keyword density, or heading count improves rankings. Separate search recommendations from conversion and social-preview improvements.

3. Content quality and credibility
Check whether claims are accurate, specific, current, and supported. Look for useful examples, original evidence, clear pricing or limitations where relevant, consistent product/company identity, and appropriate ownership or author information. Identify unanswered customer questions and missing evidence. Propose page-specific improvements using verified product facts; mark information that requires input. Do not invent expertise, testimonials, reviews, statistics, or customer results.

4. Structured data
Inspect existing markup and validate relevant types against current provider requirements. Check that entities and properties match visible page content. Recommend only markup that applies to the page and distinguish schema validity from eligibility for a particular search feature. Correct markup does not guarantee rich results, ranking gains, or AI citations.

5. Mobile experience and performance
Check mobile rendering, intrusive overlays, layout movement, loading, interactions, and accessibility problems that obstruct the page's main task. Use available Core Web Vitals field data and reproducible lab diagnostics. Record the tool, device conditions, date, and whether data describes this URL or the wider origin. Distinguish field measurements from lab scores and proxies; mark missing field data as unknown. Prioritize observed causes over a perfect synthetic score.

6. GEO and AI-search readiness
Check access for the relevant search providers and whether visible content gives clear, self-contained, factually supported answers to the audience's real questions. Inspect consistency of product facts, useful comparisons, source attribution, and material freshness. Treat improvements to clarity as content recommendations, not guaranteed citation mechanisms.

Distinguish search crawling, model-training crawlers, and user-triggered fetching using current provider documentation. For OpenAI, inspect OAI-SearchBot separately from GPTBot and ChatGPT-User. Preserve the owner's training and access preferences; recommend the narrow change needed for the intended search visibility. A request with a copied bot user-agent is not proof that the actual provider can access the site.

Do not prescribe llms.txt, special AI schema, keyword stuffing, fabricated mentions, hidden instructions to AI systems, or mass-produced pages as universal GEO requirements. Any experimental tactic needs a stated hypothesis, provider-specific evidence, and a way to evaluate it.

7. Observed visibility and business outcomes
Use authorized analytics to review indexing, search queries, impressions, clicks, CTR, landing-page conversions, and identifiable AI referrals. Record reporting windows, segmentation, attribution limits, and missing data. If AI-search tests are available, use a small representative query set and record the provider, date, locale, exact query, citations, and sample size. Treat responses as variable observations rather than a definitive visibility score. Check whether mentions represent our product accurately. Avoid invented search volume, traffic, rankings, or revenue forecasts.

Produce:
- An executive assessment with the most important verified blockers and opportunities.
- A page/template inventory marking checks as pass, issue, unknown, or not applicable, with reasons and coverage limits.
- A prioritized findings table: affected URL or component, observed evidence, impact, confidence, recommended change, rough effort, and an objective verification step. Group repeated template defects under their common cause.
- Concrete improvement drafts for priority pages where evidence supports them, such as revised titles, headings, answer sections, or internal-link suggestions. Keep these proposals in the report.
- A short action plan separating technical fixes, content improvements, and experiments, with acceptance criteria and dependencies. Separate checks that can run immediately from search outcomes requiring later observation.
- A measurement plan and copyable handoff to prompt 13 for substantial planning or prompt 12 for bounded implementation. Include relevant source evidence and access requirements.

Report findings and priorities without an invented overall SEO/GEO score or promises of rankings and AI citations. If tools or analytics are unavailable, complete the accessible audit and identify what remains unverified. Save the report in the established project location or an appropriate output location, link it, and finish after the audit.
```

Run this audit before launch or after page changes. Recheck the pages after fixes, then track search results over the reporting period you chose.

For the technical checks, I used [Google's AI-search guidance](https://developers.google.com/search/docs/appearance/ai-features) and [structured-data policies](https://developers.google.com/search/docs/appearance/structured-data/sd-policies), [OpenAI's crawler documentation](https://developers.openai.com/api/docs/bots), and the [Web Vitals guide to field and lab measurements](https://web.dev/articles/vitals).
