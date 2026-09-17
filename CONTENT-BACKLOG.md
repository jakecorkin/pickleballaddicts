# Content Pipeline — Backlog & Playbook

This file is the memory for the automated content agent that runs against this
repo. Every run should read this file first (to avoid duplicating topics and
to follow the workflow below), and update it before finishing.

## Workflow (every run)

1. Read this file. Skim `Already Published` so you don't repeat a topic or an
   angle that's already live.
2. Pick **one** topic from `Backlog`, prioritizing in this order:
   - Tips & Guides (majority of output — this is the category that scales)
   - Destinations (occasional — only when you have a genuinely well-
     researched, differentiated one; quality bar is higher here since these
     pages carry affiliate booking links)
   - Do not write Reviews or Gift Guides pages yet — out of scope until a
     human decides to expand into those categories again.
   - If the backlog is thin, propose 3–5 new candidate topics (with a one-line
     rationale each) and add them to the backlog instead of writing a page
     that run.
3. Research the topic with real web search. Every specific factual claim
   (court counts, prices, rules, specs, addresses, dates) must trace back to
   something you actually found — never invent a number or detail. If you
   can't verify a claim, cut it or soften it ("many players report...").
4. Draft the page:
   - Guides: copy the structure of `guides/pickleball-rules-for-beginners.html`
     — hero, breadcrumb, `article-layout` with `article-main` +
     `article-sidebar` (Key Takeaways + Keep Exploring links), using
     `css/guides.css`.
   - Destinations: copy the structure of an existing page in `destinations/`
     (e.g. `naples-florida.html`), using `css/destinations.css`. 600-800
     words, quick facts sidebar, related destinations.
   - Match voice: enthusiastic but not over-the-top, knowledgeable with
     specific (verified) detail, friendly, action-oriented.
   - Internal links: 2-3 minimum, pointing to relevant existing pages
     (destinations ↔ guides ↔ gift-guides).
5. Run the QA checklist below.
6. Update this file: move the topic from `Backlog` to `Already Published`,
   add any new candidate topics you noticed during research.
7. Update `sitemap.xml` with the new URL (`lastmod` = today, `changefreq` =
   monthly, `priority` 0.7).
8. Add the new page's card/listing link to the relevant index
   (`guides/index.html` or `index.html`'s destinations grid).
9. Create a branch, commit, push, and **open a PR** — do not push directly to
   `main`. Nothing publishes without a human merge. PR description should
   include the topic, why it was chosen, and sources used for factual claims.

## QA Checklist (before opening the PR)

- [ ] No leftover `PLACEHOLDER`, lorem ipsum, or TODO text
- [ ] Title tag 50-60 chars, meta description 150-160 chars
- [ ] `og:title` / `og:description` / canonical URL present and correct
- [ ] One `<h1>`, structured `<h2>`/`<h3>` hierarchy
- [ ] All images have real `alt` text (or no images used if none available)
- [ ] Affiliate disclosure box included ONLY on pages that actually contain
      affiliate/booking links — don't add it to pure informational guides
- [ ] 2-3+ internal links to existing pages
- [ ] Nav + footer on the new page match the current pattern on every other
      page (Destinations / Gift Guides / Guides / Reviews)
- [ ] Every specific factual claim is verifiable from a real source found
      during research this run
- [ ] Page added to `sitemap.xml` and to the relevant index/listing page
- [ ] Renders correctly — check locally (e.g. `python3 -m http.server`) before
      opening the PR, not just by reading the HTML

## Cadence note

The goal is **daily research, throttled publishing** — not a page live every
day. A small affiliate site that suddenly starts publishing daily reads as
"scaled content abuse" to Google, which is worse for this site than
publishing nothing. Real target: 2-4 merged posts per week. It's completely
fine, and preferred, for a run to end with "researched but decided this topic
wasn't strong enough" or "added 3 candidates to the backlog, didn't draft
anything this run."

## Research signals

No live GA4 or Search Console API access is wired up yet — this pipeline
currently runs on web search (trending topics, seasonal calendar, competitor
gap-scanning, on-site inventory) rather than real query/traffic data. Once
GA4 + Search Console API access exists, prioritize topics from actual search
queries with impressions but no ranking page over anything in this backlog.

## Already Published

_(Keep this list current — it's how future runs avoid duplicating topics.)_

**Destinations:** JW Marriott Phoenix Desert Ridge, Naples FL, Sandals
Caribbean, Palm Springs, Omni Amelia Island, Turtle Bay Oahu, San Diego &
Coronado.

**Gift Guides:** Best Pickleball Gifts for Moms, Best Pickleball Gifts for
Dads.

**Guides:** Pickleball Rules for Beginners, How to Choose Your First Pickleball
Paddle (2026-09-08), Understanding Pickleball Ratings (2026-09-09), Pickleball
Court Etiquette (2026-09-17).

## Backlog

**Tips & Guides (priority):**
- Pickleball Scoring Explained (deeper dive than the rules guide — rally
  scoring vs. traditional side-out, how to keep score in doubles). NOTE from
  2026-09-17 research: usapickleball.org is unreachable from this pipeline's
  network (egress-blocked), and web search results for this topic were
  unusually inconsistent/contradictory across secondary sources — several
  SEO sites claimed a "2026 rule change" eliminating the side-out "freeze"
  rule at game point, but this could not be corroborated against a primary
  source and other sources contradicted each other on whether Major League
  Pickleball still uses rally scoring at all. The stable core facts (11
  points, win by 2, three-number score call, doubles two-servers-per-side-out
  exception) are already covered in the rules-for-beginners guide. A future
  run should only tackle this topic if usapickleball.org (or another
  authoritative primary source) becomes reachable, or if a source search
  turns up consistent, corroborated details on the doubles serving-position
  rotation (right/left court by even/odd score) and rally-scoring specifics
  worth a dedicated "deeper dive" page.
- Pickleball vs. Tennis: Key Differences for Crossover Players
- How to Find Open Play Near You (using court-finder apps/DUPR, public parks)
- Best Practice Drills for Beginners to Improve Fast
- How to Prevent Common Pickleball Injuries (tennis elbow, ankle rolls)
- What to Wear to Play Pickleball (court shoes vs. running shoes, etc.)
- Indoor vs. Outdoor Pickleball: What Changes
- How to Care for and Maintain Your Pickleball Paddle (cleaning, storage
  temperature/humidity, when to replace grip tape — noticed while researching
  the paddle buying guide; distinct angle from buying)
- Signs It's Time to Upgrade Your Pickleball Paddle (natural follow-on for
  readers of the first-paddle buying guide a few months later)
- Pickleball Noise: Why It's Loud, What Quiet Paddles/Nets Actually Do, and
  What Cities/HOAs Require (noise ordinances are a recurring real pain point
  that came up repeatedly while researching paddle core materials; would need
  dedicated research into actual city ordinances/decibel rules before writing)
- The Third Shot Drop, Step by Step (noticed while researching skill-level
  definitions for the ratings guide — this single shot is what separates a
  3.0 from a 3.5/4.0 player and repeatedly came up as its own topic in
  competitor content; would pair well with a follow-on dinking guide)
- Pickleball Dinking: How to Win the Kitchen-Line Battle (same research
  trail as the third shot drop — dinking is the other skill that
  consistently defines the jump from 3.0 to 4.0)
- How to Get Started with DUPR (practical follow-on to "Understanding
  Pickleball Ratings" — creating a profile, which clubs/apps auto-sync
  results, how to log a casual match yourself)
- Pickleball "Stacking" Strategy Explained (doubles positioning strategy where
  partners line up on the same side before a serve/return to keep a
  favored player on their stronger side — noticed while researching court
  etiquette that "stacking" is a confusingly overloaded term: the etiquette
  guide covers the unrelated paddle-queue meaning, and a dedicated strategy
  guide would resolve the ambiguity while covering real intermediate-level
  content)

**Destinations (occasional, high bar):**
- Austin, TX pickleball scene
- Scottsdale/Phoenix broader metro (distinct from the existing JW Marriott
  page — city-wide public courts angle)
- Las Vegas pickleball resorts
- Myrtle Beach, SC

**Needs more research before adding to backlog:** none currently — add
candidates here as they come up.
