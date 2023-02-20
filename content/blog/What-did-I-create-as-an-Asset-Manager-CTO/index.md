---
title: "What Did I Create as an Asset Manager CTO"
date: 2022-09-12T14:32:09-04:00
draft: false
---

In this post, I am going to share what I built as [CTO](https://noverse.com/blog/2012/10/05/the-hedge-fund-cto-role/) for the three Asset Managers I worked for over the past 22 years. I have created this page as a result of people asking for more information on what I actually did build, now that I have moved on from my third role.

In each case, these Asset Managers started as "green fields" startups. Using the technology I created for them, they grew from almost nothing to nearly billion dollar managers.

In each case, I:

- Designed and created the platform architecture and structure from scratch to meet and exceed the goals and strategies of each Manager, from front-to-back across all aspects of the business
- Designed, coded and tested the major components, often single-handedly until the asset base grew, writing hundreds of thousands of lines of readable and maintainable code
- Proved the numbers and calculation results in all cases, and certified these systems with counter-parties to ensure correctness, reliability and performance at all times
- Launched these products into production, ran them as the critical business backbone of each Manager, enhanced and supported these products with *six-nines* uptime, and used them successfully as a trader and operations user
- Brought in a small team of talented developers to help grow and expand these product capabilities and coverage
- In some cases, evolved a second version to radically increase the capabilities of the Manager
- Learned, followed and proved the utility of a bunch of themes that enabled me to design, build and evolve the products better, quickly and easily — see [Hiltmonisms](https://hiltmon.com/tags/hiltmonism/) on [Hiltmon.com](https://hiltmon.com/) for details of these themes

There are some topics and details I cannot share, but the below is a high-level overview.

## Asset Manager 3: Fixed income automated algorithmic trading platform

My latest Manager was the first to trade certain fixed income security instruments electronically and algorithmically, becoming one of the top five electronic volume traders on fixed income exchanges. The platform is multi-asset, multi-fund, multi-user, multi-* ensuring the Manager could run tens of thousands of securities in each portfolio within their unique mandates.

*The competitive advantage of this platform was the sheer breadth of visibility into markets and liquidity, and the ability to rapidly take automated advantage of opportunities in the market.*

The platform I built included:

- A data platform to ingest and store massive volumes of data including security master, pricing, prints, observations, baskets, constituents, live time-series ticks and parsed runs, data being both real time and historical, all stored in a single normalized, consistent database across fixed income and non-fixed income asset classes
- A calculation engine that rapidly ran hundreds of millions of calculations a day for all fixed income risk, analytics and derived data, with all numbers proven correct
- A market data connectivity platform to build, aggregate and maintain live order books, needed for real time trading
- A connectivity layer to integrate and normalize almost all fixed income (and some non-fixed income) exchanges supporting all their workflows, from live market trading (passive and aggressive orders), Request for Quotation flow (incoming and outgoing), direct connect trading, drop copies, non-fixed income orders and fills and any other flows supported by these vendors
- An order and execution management system (OEMS) to act as the core engine of the business, upstream of the connectivity, enabling and managing all trade flows, compliance, cash and fees, business rules and even making execution decisions, processing millions of messages a day and providing a massive competitive advantage to the Manager
- A set of Graphical User Interfaces to enable users to visualize markets, security analytics, trading activity, performance attribution and to trade manually
- A middle and back office platform to handle allocations, generate profit and loss, integrate with the myriad of administrators, prime brokers and separately managed account managers, designed to save headcount by automating the operational processes and providing information to enable operations by exception
- A real-time algorithmic hosting container that provided a real-time, live market and data view to enable fully automated trading, across all markets and flows, with complex business logic, using the downstream OEMS to execute and share the state of orders
- And all the other bits and bobs needed to support this platform, from infrastructure, through data modeling, live rates, cyber-security, dev-ops, reporting, risk calculation and management, APIs, simulations, etc.

## Asset Manager 2: Broad multi-asset manager, moving liquidity amongst all markets based on performance

The Manager before was a unique one, it wanted to trade all asset classes in the market on a single platform and the thesis was to move capital allocation to the "hot" markets while remaining active in all. In the end, the platform I built supported 65 asset classes, from equities, fixed-income, futures, options, derivatives, rate of return baskets,  mortgages, whole loans, structured products and everything in-between. For more details on this old architecture, see [A Hedge Fund Technology Architecture](https://noverse.com/blog/2013/05/06/a-hedge-fund-technology-architecture/).

*The competitive advantage of this platform was the flexibility to trade any asset class at any time to take advantage of market moves.*

The platform I built included:

- A core library of business logic and normalizations to enable abstraction and trading of all asset classes under a single umbrella
- A front office platform to enable visualization, trading and operations across all asset classes, including OTC creation, electronic and manual trading, ticket capture, post trade operations, trader book reviews and a large number of portfolio reports
- A middle layer that ensured all data in the platform was normalized and routed to where it needed to be including risk systems, trader analytics, back office, prime brokers, administrators and clearing houses
- A back office component to manage cash, holdings, allocations, margin, reconciliations, P&L, repo and financing, and all other administrative functions
- A risk and analytic platform to calculate, consolidate and present numbers from fixed income engines, mortgage tools, equity analytics and end of day risk systems
- And of course, the data loaders, data model, third-party integrations, pricing models, valuation models, analytics, investor management and other dependencies a platform this broad needed

## Asset Manager 1: A Japanese/US fixed income and derivatives manager

Building this platform is where I started to learn the business of asset management and the art of trading, especially since several of the principals were senior professors at world-renowned universities, and the traders came off the desks you read about in good books.

*The competitive advantage of this platform was the ability to electronically trade in mostly manual markets and to do so across jurisdictions without hassle.*

There I built my first full front-to-back platform, including:

- Trade blotter to capture both Japanese and USA trading in fixed income, futures, derivatives and other asset classes
- A full and comprehensive back office platform based on an accounting model to support profit and loss, net asset value and all operations flows and integrations
- Was amongst the first to electronically trade in both the USA and Japan in a variety of asset classes with many vendors
- Was amongst the first to apply automated and algorithmic models to automated, cross-national trading, writing our own pricing models
- Was amongst the first to provide full investor reporting transparency, allowing investors to log securely into a public web site to see and download their daily performance and NAV
- Integration with risk systems and regulatory systems and the ability to automate hedging and financing transactions

## How did I manage all this?

*Or in other words, how come these projects did not fail like most large, complex, broad IT projects?*

Some of it was experience, but a lot of it was learning and understanding the market and flows being designed and implemented, and in actually performing the roles of trader and operations. It helped a lot that I had direct access to the critical personnel at all times. The secret to success here came from:

- Having already spent 10 years previously learning to architect, design and build complex business products surrounded by great mentors (and in seeing — and learning from — a bunch of project failures)
- Having direct access to the books and people who knew the business best and in being able to spend time and ask deep questions on what and why they did things (and to patiently listen to my ideas on how to do things better)
- Keeping the architectures and code simple to enable more rapid development, easy maintenance and logical enhancement
- Talking the time to try out new ideas, languages, patterns and architectures (and in having managers who gave me the freedom to do so)
- Releasing early and often, growing the platform in full view and with the full support and sometimes brutal feedback from the team who used it
- Making mistakes, learning from them, proving and certifying deliverables and building trust in the platform, and then making the platform invisible ("it just works") allowing users to focus on their work and not on the tools
- Ensuring the evolution of the platform removed constraints and barriers to the business instead of creating them
- Finding my limits and then hiring talented, experienced developers with diverse skills and mind-sets, training them up in the business, flows and themes, and finally trusting and freeing them grow from there
- And in building on my growing expertise and confidence to rapidly create more intelligent and capable systems to accelerate the capabilities of each Manager

And now I have all this confidence, experience and a bounty of ideas on what can be done and how to do it better, smarter, and faster to drive even more business opportunities and capabilities.

Which is pretty much where we all are, and should be, in the middle of our careers.
