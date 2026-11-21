I'm a full-stack engineer in M'saken, Tunisia. I build web and mobile products with React, Next.js, TypeScript, Laravel and React Native, and I like owning the whole product, from the API to the phone app. [A restaurant I co-founded](https://www.facebook.com/ghostchef.tn) ran on the platform I wrote by hand, at 200+ orders a day at peak.

Now I'm a software engineer at Decade, on high-traffic French e-commerce sites. Before that I worked on the [Mobility Data Space connector UI](https://github.com/Mobility-Data-Space/mds-edc-ui) at Think-it, and on client projects at Anypli.

## Projects

- **[GhostChef](https://github.com/mkhinini-motaz/ghostchef)**: a food-ordering platform, written by hand from 2019 in Laravel, React, React Native and MySQL ([code](https://github.com/stars/mkhinini-motaz/lists/ghostchef)). The restaurant ran on it from 2021 to 2023.
- **GhostChef delivery platform**: the rebuild I started in 2026 with Claude Code, in development and private. [Case study](https://github.com/mkhinini-motaz/ghostchef).
  - A Laravel API; Next.js and MUI web apps for admins, shops and customers; four React Native apps for customers, merchants, riders and admins; a Socket.IO realtime server.
  - 364 test files in the API and 366 across the phone apps.
- **[Car Rental](https://github.com/mkhinini-motaz/car-rental)**: software to run a small car rental agency in Tunisia (fleet, bookings, contracts, cash book). Built with Claude Code.
  - Laravel API, React Native staff app and Next.js web app; 135 web and 99 API tests; CI.
  - Five UI languages, among them Arabic and two forms of Tunisian Arabic. Car handover works offline on the phone, and money is stored in integer millimes, never floats.
- **[simulate](https://github.com/mkhinini-motaz/simulate)**: a Claude Code skill built from GhostChef's town simulator. Bots play an app's users against an isolated copy, and a finding counts only when a failing test proves it.
- **First Car Rental** ([app](https://github.com/mkhinini-motaz/car), [API](https://github.com/mkhinini-motaz/carapi)): the same idea, written by hand from 2024 to 2025.
- **[msk-log](https://www.npmjs.com/package/msk-log)**: a small npm logger from 2018 that colours console output and can write it to a file.

## Work

- **Decade**, since 2025: software engineer on e-commerce sites for major French retailers, with React, Next.js and TypeScript. Product, search and listing pages, and the shared components behind them, in a team of about 40.
- **Think-it**, 2024 to 2025: the MDS connector UI, a Gaia-X project funded by the German Federal Ministry of Transport. Server-side rendering, SEO, Playwright end-to-end tests and code reviews.
- **GhostChef restaurant**, 2021 to 2023: co-founder. I was the sole technical lead and also ran operations: clients, suppliers, marketing and finances.
- **Anypli**, 2018 to 2022: full-stack work with Laravel, MySQL, React, Next.js, Vue.js and Nuxt. Anypli placed me with client teams such as Webdentiste and Rise Up, and I led the technical side of client projects.
- **Subvitamine**, near Montpellier, France, 2018: my final-year engineering internship.

## How I build

- **Test before users do.** GhostChef has a simulated town where bots place orders.
- **Small UI details count,** in Arabic as well as in French and English.
- **Lean infrastructure.** My first GhostChef server was one DigitalOcean droplet at 5 USD a month that I configured myself.
- **Code that holds up:** SOLID, the framework's best practices, no wasted queries. I think about attackers before launch.
- **Look around first.** I study competitors at home and abroad before I build, and I look for the opposite view before I decide.

## Claude Code

For my own projects I tune Claude Code and measure each change on my session transcripts. I decide what to measure and change; Claude Code writes most of the scripts, which are public in [claude-code-session-toolkit](https://github.com/mkhinini-motaz/claude-code-session-toolkit).

- Up to 32% fewer main-thread tokens by compacting at 300k tokens instead of 400k, and up to 30% fewer subagent tokens at 200k (a replay of my transcripts, so upper bounds).
- 13% lower cost from two plugins for terse answers and minimal code, in a blind A/B test of 16 runs with the same graded quality.
- 44% smaller rules files across 10 repositories: I moved narrative into notes that load on demand, and a hook blocks any file over 40,000 bytes.
- About 9% less starting context: skills unused for 30 days show by name only, which saves about 6k tokens a session.
- A token report from my transcripts showed that subagents used 65% of input tokens. In one session, 221 agent wake-ups made up 70% of the main thread, so I now limit large fan-outs.
- An eval suite scores my advisor agents' answers ([founder-advisors](https://github.com/mkhinini-motaz/founder-advisors)) against a checklist, next to a baseline without the advisor.
- Two popular tools didn't fit my setup. That says nothing against them, and many people use both:
  - [rtk](https://github.com/rtk-ai/rtk) compresses command output. On 250 of my real commands it saved 0.1% of input tokens.
  - [OmniRoute](https://github.com/cheaper-inference/OmniRoute) runs Claude Code on free models. Their rate limits stopped my full sessions, and some free tiers train on prompts, which rules them out for my private code.

## Stack

TypeScript, JavaScript, PHP; React, Next.js, React Native, React Query, Redux, Vue.js, Nuxt, MUI, Tailwind; Laravel, MySQL, Redis, Socket.IO; Docker, Git, Playwright.

Arabic (native), French (C1), English (professional working), German (elementary).

Outside work: video games, food and restaurants (enough to co-found one), and reading about startups and their founders. [LinkedIn](https://www.linkedin.com/in/moatez-mkhinini)
