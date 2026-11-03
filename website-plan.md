# Website Plan: "IssueSolver" — People's Issues Resolution Platform

## 1. Vision
A web platform where users submit real-life issues (legal, financial, health, tech, daily life) and get structured, actionable solutions from verified experts + community + AI triage.

## 2. Core Pages
- Home — hero, search bar, issue categories, success stories
- Submit Issue — guided form with category, severity, attachments
- Issue Feed — filterable list with status, upvotes, expert replies
- Issue Detail — thread, expert answers, status timeline, related issues
- Expert Directory — profiles, ratings, availability
- Dashboard — my issues, saved, notifications
- Admin Panel — moderation, category management, analytics

## 3. Tech Stack (recommended)
- Next.js 14 (App Router) + TypeScript
- Tailwind CSS + shadcn/ui
- Prisma + PostgreSQL
- NextAuth (email + Google)
- tRPC or Server Actions for API
- UploadThing / S3 for attachments
- Resend for email notifications

## 4. Data Model
- User (id, name, role: user/expert/admin, reputation)
- Issue (id, userId, category, title, body, severity, status, votes)
- Response (id, issueId, authorId, body, isExpert, accepted)
- Category (id, name, icon, slug)
- Review (id, expertId, userId, rating, comment)

## 5. Key Features
- AI pre-triage: auto-categorize + suggest existing solutions before posting
- Expert matching by category + availability
- Status flow: Open → In Progress → Resolved → Closed
- Voting + "solution accepted" badge
- Reputation system for experts
- Email + in-app notifications
- Search with filters (category, status, date, severity)

## 6. MVP Phases
- Phase 1 (2 wks): Auth, submit issue, feed, detail page
- Phase 2 (2 wks): Expert replies, voting, status flow
- Phase 3 (2 wks): Expert directory, dashboard, notifications
- Phase 4 (1 wk): AI triage, search, polish, deploy

## 7. Design Direction
- Clean, trust-building UI: blues/greens, high contrast
- Mobile-first, accessible (WCAG AA)
- Card-based issue feed, clear status badges
- Expert profiles with credibility indicators

## 8. Next Steps
1. Set up Next.js project + Prisma schema
2. Build auth + issue CRUD
3. Design component library (shadcn)
4. Deploy to Vercel with Postgres
