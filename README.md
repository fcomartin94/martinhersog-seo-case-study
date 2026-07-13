# Technical SEO Audit — martinhersog.com

*[Leer en español](README.es.md)*

**Client:** María Martín Hersog ([martinhersog.com](https://martinhersog.com))
**Project type:** Technical SEO audit and optimization
**Scope:** WordPress + RankMath SEO + Google Search Console

## Short description

Technical SEO audit and optimization for María Martín Hersog's professional portfolio
(martinhersog.com): installed and configured RankMath, verified the site in Google
Search Console, fixed heading structure issues, and optimized metadata and image
accessibility. On-page SEO score improved from **78 to 91/100**.

---

## Context

María Martín Hersog is a graphic and web designer with a WordPress portfolio that has
been live since 2021 but had never had any technical SEO work done. The site had no
SEO plugin installed, was not verified in Google Search Console, and had several
technical structure issues that made it harder for search engines to index and
interpret the content. Built with WordPress + the Salient theme + WPBakery Page
Builder.

## Goal

Establish a solid technical SEO foundation to build on in the future with a content
and visibility strategy — leaving the site correctly configured, measurable, and free
of structural errors, even though the direct impact on search traffic depends on
follow-up work (content, external links).

**Access note:** the site owner offered full access to the hosting account; for
security, that direct access was not used. Instead, work was done through a separate,
limited administrator account created within WordPress.

## Work done

### 1. Tooling setup

- Installed and configured **RankMath SEO** (no SEO plugin was present before).
- Created a property in **Google Search Console** and verified it.
- **Issue found:** HTML tag verification kept failing — the code published in the
  site's `<head>` didn't match the one RankMath was inserting, a sign that another
  source had priority. Ruled out the RankMath plugin, caching, and other installed
  plugins as the cause (disabling them one by one). The exact origin was never
  pinpointed (likely an old meta tag hardcoded in the parent theme), but that didn't
  block the fix.
- **Fix applied:** verification via Search Console's alternative **"HTML file"**
  method, which doesn't compete for the site's `<head>` — worked on the first try.

### 2. Technical structure fixes

- **Duplicate H1 on the homepage:** the heading module had 3 `<h1>` tags on the same
  page (there should be exactly 1). Cause: two additional headings were manually
  hardcoded as `<h1>` in the content block instead of `<h2>`. Fixed by changing the
  heading level of those two elements.
- **Exposed author sitemap:** WordPress's native sitemap included a `users`
  sub-sitemap, needlessly exposing the site's usernames — no SEO value and a minor
  security risk. Resolved automatically once RankMath was activated, as it took over
  sitemap generation and disabled WordPress's native one.
- **Images missing alt text:** wrote descriptive alt text for 60+ images across the
  portfolio, covering both the ones flagged by RankMath's analyzer and the rest of the
  project catalog — improving both accessibility and image SEO.

### 3. On-page optimization

- Wrote SEO titles and meta descriptions for the site's 4 main pages (Home, About,
  Portfolio, Contact).
- Defined a target keyword for the 4 main pages and the 14 individual portfolio
  entries.
- Adjusted internal page titles (WordPress) to align with the target keywords — with
  care taken because, on this site, the navigation menu automatically inherits a
  page's title as its menu label unless that field has been customized manually. The
  menu label was set manually in each case to avoid breaking the menu's visual
  consistency.

## Results: on-page SEO score progression (RankMath)

| Stage | Score | Detail |
|---|---|---|
| First full report | 78/100 | 21 tests passed / 1 warning / 4 failures |
| After H1, images, titles and keywords | 86/100 | 22 tests passed / 1 warning / 3 failures |
| After portfolio keywords and final adjustments | **91/100** | 23 tests passed / 0 warnings / 3 failures |

The remaining failures at the close of this phase are lower-impact and documented as
follow-ups: 14 portfolio entries where the keyword doesn't yet appear in the WordPress
internal title (same fix already applied to the 4 main pages), incomplete OpenGraph
tags, and a one-off mobile speed test execution failure (a tooling issue, not a site
issue).

## Methodology note

This work covers technical and on-page SEO — site hygiene and structure, not
promotion or traffic generation. Its value is providing a correctly built foundation
for future content and visibility work, which is what will ultimately drive real
search ranking impact for competitive terms.

## Next steps for a future phase

- Expand the main pages' content (target 600+ words) integrating the keyword
  naturally, to raise the real score beyond metadata adjustments.
- Adjust the WordPress internal title of the 14 portfolio entries.
- Complete OpenGraph tags to improve link previews when sharing on social media.
- Install Google Analytics as a second property-verification method and to start
  collecting traffic data.
