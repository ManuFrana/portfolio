# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Single static HTML file (`index.html`) with inline CSS/JS. User's explicit choice over Astro
and Next.js. No build step, no dependencies, no framework — deployable by dropping one file
on GitHub Pages, Netlify or Vercel. Assets (CV PDF, Catox screenshots) sit beside it.

## Users

**Primary:** recruiters, technical hiring managers and engineering leads evaluating Manuel
Frana for Senior QA Automation / SDET and backend engineering roles, primarily in Spain, the
EU and remote-first companies.

**Their situation:** they arrive from a LinkedIn profile link, a CV footer or a direct message,
usually mid-screening with a stack of other candidates open. Frequently on a phone. They give
the page well under a minute on first contact.

**Their job:** decide within that minute whether Manuel is worth a call, and leave with the CV
PDF in hand. A secondary, slower visit happens when a technical interviewer returns to look at
the actual engineering work before a conversation.

## Product Purpose

One public URL that does three things without the visitor hunting: says what Manuel does, hands
over the CV PDF in a single click, and proves the claim with real engineering artifacts.

Success is a recruiter downloading the CV or opening LinkedIn, and a technical interviewer
arriving at the call already knowing about Catox or Courts.

## Positioning

Manuel is a Senior QA Engineer who ships production code. On Avature's Framework team — the
proprietary backend layer (database access, Redis caching, metrics registration) that ~40
product teams build on — he finds the gap, writes the specification, and implements it himself.
Because the platform runs on an in-house framework, he builds the test harnesses, instrumentation
and release tooling that off-the-shelf frameworks would otherwise supply.

The claim a neighboring QA candidate could not truthfully copy: he owns a progressive production
rollout across client instances, and his personal project enforces its own architecture with an
automated test that fails the build when code bypasses the security gateway.

## Operating Context

- Visitors arrive from LinkedIn, a CV link, or a forwarded URL. There is no marketing funnel,
  no search traffic to court, and no returning-user session.
- The page is frequently forwarded between a recruiter and a hiring manager, so it must stand
  alone without Manuel present to narrate it.
- The CV PDF is compiled from `Manuel_Frana_CV.tex` (Jake's Resume template) on Overleaf and
  placed beside `index.html`. There is no local LaTeX toolchain.
- Job titles matter for scanning: the visitor is matching against a req that says "Senior QA
  Engineer", "SDET" or "Test Automation Engineer".

## Capabilities and Constraints

- Fully static. No backend, no database, no server-side rendering, no contact form.
- No analytics tooling decided. Do not add tracking without asking.
- Must work well on a phone; recruiters open these links on mobile constantly.
- **Undecided:** the deploy target (GitHub Pages / Netlify / Vercel) and therefore the final
  public URL. Do not hardcode a domain.
- **Undecided:** whether the Courts and Catox GitHub repositories will be made public. Until
  confirmed, the page must not link to repository URLs that may 404.

## Brand Commitments

- Name: **Manuel Frana**. Professional title: **Senior QA Automation Engineer | SDET**.
- Contact surface is deliberately limited to three items, confirmed by the user:
  **manuel.frana@hotmail.com**, **linkedin.com/in/franamanuel**, **github.com/ManuFrana**.
- **Phone number and location are excluded from the public page by explicit decision** (scraping
  and cold-calling). The phone lives on the PDF only. Do not reintroduce either.
- Page language is English, matching the CV and the target market.
- No existing logo, wordmark, personal palette or prior personal site to inherit from.

## Evidence on Hand

**Real, usable:**
- Six 1913×901 gameplay screenshots of Catox at `C:\Users\manue\Pictures\Screenshots\`:
  `catox-board.png` (hex island, no Roblox chrome — the cleanest), `catox-top-view.png`,
  `catox-first-person.png` (walkable 3D island with player-built settlements),
  `catox-create-trade.png` and `catox-receive-trade.png` (the React/Rodux trade UI),
  `catox-store.png`.
- Catox source at `C:\Users\manue\Desktop\Roblox Dev\Proyects\catox`: ~49K LOC Luau, 67
  `.spec.luau` files, a Command-pattern gateway (`CommandGateway`, `EventDispatcher`,
  `SuspicionLog`), and `tests/Gateway/NoDirectFireClient.spec.luau` — an architectural test that
  fails the suite if any code calls `:FireClient` outside the dispatcher.
- Courts source at `C:\Users\manue\Desktop\Personal\Courts`, including a real written incident
  `POSTMORTEM.md` (session-token mismatch across HTTP clients) and `test/test_availability.py`.
- `Manuel_Frana_CV.tex` — the full, placeholder-free CV.

**Absences future work must not fabricate:**
- Catox is **live but private** on Roblox and not yet publicly launched. There is no playable
  link, no player count, no revenue, no store metrics, no reviews.
- No testimonials, references, client logos, press or awards exist.
- No employer-verified figures beyond those Manuel confirmed for the CV (~40 product teams
  consuming the framework; up to 50% test-suite runtime reduction; 2 QA engineers coordinated).
- Manuel has no 3D modelling skill; Catox's visual assets are sourced, not authored by him.
  Do not present him as an artist.

## Product Principles

1. **The PDF is the conversion.** Every layout decision answers to whether a rushed recruiter
   can get the CV in one click from any scroll position.
2. **Prove, don't adjective.** "Detail-oriented" is worthless; a test that fails the build when
   someone bypasses the gateway is not. Lead with artifacts.
3. **Two audiences, one page.** A recruiter scanning for 45 seconds and an engineer reading for
   ten minutes must both be served without the page forcing either into the other's path.
4. **Never outrun the evidence.** No invented metrics, no implied launch, no borrowed
   credibility. The real material is strong enough.
5. **One file, no rot.** This page must still deploy unchanged in three years with no dependency
   upgrades, so it stays a job-search asset instead of a maintenance chore.

## Accessibility & Inclusion

Mobile-first is a hard requirement, not a nicety — a large share of first contacts open the link
on a phone. Keyboard navigation and visible focus states are required: this page exists to be
forwarded and used by people whose setups Manuel cannot predict.
