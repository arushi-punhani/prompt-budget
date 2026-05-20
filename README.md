# PromptBudget

Audit AI tool subscriptions and identify wasted spend instantly.

PromptBudget is a free web app that analyzes a team’s AI tooling stack, detects overspending, and recommends cheaper plans or alternative tools based on actual usage patterns. Users receive an instant audit with estimated monthly and annual savings, plus a shareable public report URL.

---

# Features

## MVP Features

* AI tool spend input form
* Persistent form state across reloads
* Rule-based audit engine
* Per-tool optimization recommendations
* Monthly + annual savings calculations
* AI-generated personalized summary
* Shareable public audit URLs
* Open Graph preview support
* Lead capture with backend storage
* Transactional confirmation email
* Abuse protection

---

# Supported Tools

## Current Supported Vendors

* Cursor
* GitHub Copilot
* Claude
* ChatGPT
* Anthropic API
* OpenAI API
* Gemini
* Windsurf

Each tool supports:

* plan selection
* monthly spend input
* seat count

Additional inputs:

* team size
* primary use case

  * coding
  * writing
  * data
  * research
  * mixed

---

# Screenshots

## Landing Page

# PromptBudget

Audit AI tool subscriptions and identify wasted spend instantly.

PromptBudget is a free web app that analyzes a team’s AI tooling stack, detects overspending, and recommends cheaper plans or alternative tools based on actual usage patterns. Users receive an instant audit with estimated monthly and annual savings, plus a shareable public report URL.

Built as part of the Credex engineering assignment.

---

# Features

## MVP Features

* AI tool spend input form
* Persistent form state across reloads
* Rule-based audit engine
* Per-tool optimization recommendations
* Monthly + annual savings calculations
* AI-generated personalized summary
* Shareable public audit URLs
* Open Graph preview support
* Lead capture with backend storage
* Transactional confirmation email
* Abuse protection

---

# Supported Tools

## Current Supported Vendors

* Cursor
* GitHub Copilot
* Claude
* ChatGPT
* Anthropic API
* OpenAI API
* Gemini
* Windsurf

Each tool supports:

* plan selection
* monthly spend input
* seat count

Additional inputs:

* team size
* primary use case

  * coding
  * writing
  * data
  * research
  * mixed

---

# Screenshots

## Landing Page


## Spend Input Form



## Audit Results Page



## Optional Demo Video



# Tech Stack

## Frontend

* Next.js 15
* React
* TypeScript
* Tailwind CSS
* shadcn/ui

## Backend

* Next.js Route Handlers
* Supabase

## AI

* Anthropic API

## Deployment

* Vercel

## Email

* Resend

---

# Quick Start

## 1. Clone the repository

```bash
git clone https://github.com/yourusername/promptbudget.git
cd promptbudget
```

---

## 2. Install dependencies

```bash
npm install
```

---

## 3. Configure environment variables

Create a `.env.local` file:

```env
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_ROLE_KEY=
ANTHROPIC_API_KEY=
RESEND_API_KEY=
NEXT_PUBLIC_BASE_URL=
```

---

## 4. Run locally

```bash
npm run dev
```

App runs at:

```txt
http://localhost:3000
```

---

## 5. Run tests

```bash
npm run test
```

---

# Project Structure

```txt
app/
components/
lib/
pricing/
public/
tests/

README.md
ARCHITECTURE.md
DEVLOG.md
REFLECTION.md
TESTS.md
PRICING_DATA.md
PROMPTS.md
GTM.md
ECONOMICS.md
USER_INTERVIEWS.md
LANDING_COPY.md
METRICS.md
```

---

# How It Works

## 1. User submits AI stack

The user enters:

* tools
* plans
* monthly spend
* seat counts
* use case

---

## 2. Audit engine evaluates spend

The audit engine uses deterministic rules to evaluate:

* plan fit
* redundant tools
* cheaper alternatives
* overprovisioned team plans
* overlapping functionality
* API vs subscription tradeoffs

The logic is intentionally rule-based instead of AI-generated so recommendations remain explainable and financially defensible.

---

## 3. Personalized AI summary

An LLM generates a concise personalized summary of the audit.

If the API fails:

* a deterministic fallback summary is returned
* the audit still completes successfully

---

## 4. Public report generation

Each audit receives:

```txt
/report/[slug]
```

Public reports:

* remove identifying information
* preserve tool and savings data
* generate Open Graph previews for sharing

---

# Audit Engine Philosophy

PromptBudget intentionally avoids using AI for core financial recommendations.

The audit engine is based on:

* transparent rules
* current pricing data
* explainable recommendations
* usage-fit reasoning

Example:

```txt
ChatGPT Team for 2 users may be overprovisioned.
Downgrading to Plus reduces spend while preserving core functionality.
```

This approach improves:

* trustworthiness
* reproducibility
* pricing accuracy
* debugging simplicity

---

# Abuse Protection

PromptBudget includes:

* basic rate limiting
* honeypot spam detection
* server-side validation

This prevents:

* automated spam submissions
* API abuse
* excessive LLM requests

---

# Performance Goals

The application targets:

* Lighthouse Performance ≥ 85
* Accessibility ≥ 90
* Best Practices ≥ 90

Optimizations include:

* server rendering
* lightweight components
* minimal client-side state
* optimized images
* cached pricing data

---

# Decisions

## 1. Deterministic audit engine instead of AI recommendations

The audit calculations are rule-based because financial recommendations should be explainable and reproducible.

---

## 2. No authentication

Removing signup friction improves completion rates and supports the product’s viral sharing loop.

---

## 3. LocalStorage persistence

Form state persists across refreshes without requiring accounts or backend sessions.

---

## 4. Next.js instead of separate frontend/backend services

Using a unified framework simplified deployment, reduced infrastructure complexity, and improved iteration speed.

---

## 5. Public shareable reports

Public URLs create a built-in viral acquisition loop through screenshots and social sharing.

---

# Future Improvements

* PDF export
* Benchmarking against similar companies
* Browser extension for subscription detection
* Spend trend tracking
* Referral system
* Embeddable widget version
* Multi-user collaboration

---

# Deployment

## Vercel Deployment

Deploy using:

```bash
vercel
```

Environment variables must be configured in:

* Vercel Project Settings

---

# Live Demo

```txt
https://your-live-url.vercel.app
```

---

# Documentation

Additional project documentation:

* ARCHITECTURE.md
* DEVLOG.md
* REFLECTION.md
* TESTS.md
* PRICING_DATA.md
* PROMPTS.md
* GTM.md
* ECONOMICS.md
* USER_INTERVIEWS.md
* LANDING_COPY.md
* METRICS.md

---

# License

MIT License

![Audit Results](./public/screenshots/results.png)
```

---

## Optional Demo Video

Loom / YouTube link:

```md
https://your-demo-link.com
```

---

# Tech Stack

## Frontend

* Next.js 15
* React
* TypeScript
* Tailwind CSS
* shadcn/ui

## Backend

* Next.js Route Handlers
* Supabase

## AI

* Anthropic API

## Deployment

* Vercel

## Email

* Resend

---

# Quick Start

## 1. Clone the repository

```bash
git clone https://github.com/yourusername/promptbudget.git
cd promptbudget
```

---

## 2. Install dependencies

```bash
npm install
```

---

## 3. Configure environment variables

Create a `.env.local` file:

```env
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_ROLE_KEY=
ANTHROPIC_API_KEY=
RESEND_API_KEY=
NEXT_PUBLIC_BASE_URL=
```

---

## 4. Run locally

```bash
npm run dev
```

App runs at:

```txt
http://localhost:3000
```

---

## 5. Run tests

```bash
npm run test
```

---

# Project Structure

```txt
app/
components/
lib/
pricing/
public/
tests/

README.md
ARCHITECTURE.md
DEVLOG.md
REFLECTION.md
TESTS.md
PRICING_DATA.md
PROMPTS.md
GTM.md
ECONOMICS.md
USER_INTERVIEWS.md
LANDING_COPY.md
METRICS.md
```

---

# How It Works

## 1. User submits AI stack

The user enters:

* tools
* plans
* monthly spend
* seat counts
* use case

---

## 2. Audit engine evaluates spend

The audit engine uses deterministic rules to evaluate:

* plan fit
* redundant tools
* cheaper alternatives
* overprovisioned team plans
* overlapping functionality
* API vs subscription tradeoffs

The logic is intentionally rule-based instead of AI-generated so recommendations remain explainable and financially defensible.

---

## 3. Personalized AI summary

An LLM generates a concise personalized summary of the audit.

If the API fails:

* a deterministic fallback summary is returned
* the audit still completes successfully

---

## 4. Public report generation

Each audit receives:

```txt
/report/[slug]
```

Public reports:

* remove identifying information
* preserve tool and savings data
* generate Open Graph previews for sharing

---

# Audit Engine Philosophy

PromptBudget intentionally avoids using AI for core financial recommendations.

The audit engine is based on:

* transparent rules
* current pricing data
* explainable recommendations
* usage-fit reasoning

Example:

```txt
ChatGPT Team for 2 users may be overprovisioned.
Downgrading to Plus reduces spend while preserving core functionality.
```

This approach improves:

* trustworthiness
* reproducibility
* pricing accuracy
* debugging simplicity

---

# Abuse Protection

PromptBudget includes:

* basic rate limiting
* honeypot spam detection
* server-side validation

This prevents:

* automated spam submissions
* API abuse
* excessive LLM requests

---

# Performance Goals

The application targets:

* Lighthouse Performance ≥ 85
* Accessibility ≥ 90
* Best Practices ≥ 90

Optimizations include:

* server rendering
* lightweight components
* minimal client-side state
* optimized images
* cached pricing data

---

# Decisions

## 1. Deterministic audit engine instead of AI recommendations

The audit calculations are rule-based because financial recommendations should be explainable and reproducible.

---

## 2. No authentication

Removing signup friction improves completion rates and supports the product’s viral sharing loop.

---

## 3. LocalStorage persistence

Form state persists across refreshes without requiring accounts or backend sessions.

---

## 4. Next.js instead of separate frontend/backend services

Using a unified framework simplified deployment, reduced infrastructure complexity, and improved iteration speed.

---

## 5. Public shareable reports

Public URLs create a built-in viral acquisition loop through screenshots and social sharing.

---

# Future Improvements

* PDF export
* Benchmarking against similar companies
* Browser extension for subscription detection
* Spend trend tracking
* Referral system
* Embeddable widget version
* Multi-user collaboration

---

# Deployment

## Vercel Deployment

Deploy using:

```bash
vercel
```

Environment variables must be configured in:

* Vercel Project Settings

---

# Live Demo

```txt
https://your-live-url.vercel.app
```

---

# Documentation

Additional project documentation:

* ARCHITECTURE.md
* DEVLOG.md
* REFLECTION.md
* TESTS.md
* PRICING_DATA.md
* PROMPTS.md
* GTM.md
* ECONOMICS.md
* USER_INTERVIEWS.md
* LANDING_COPY.md
* METRICS.md

---

# License

MIT License

