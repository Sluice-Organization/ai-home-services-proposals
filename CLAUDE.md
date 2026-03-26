# AI Proposal Generator for Home Service Contractors

## Product Overview
AI Proposal Generator for Home Service Contractors is a SaaS platform that helps plumbers, electricians, HVAC technicians, roofers, landscapers, and other home service professionals create polished, accurate proposals in minutes instead of hours. The platform uses AI to take rough job notes, photos, and scope descriptions and turn them into professional, branded proposals complete with pricing, timelines, material lists, and terms - ready to send to homeowners for e-signature. Over time, the AI learns each contractor's pricing patterns, preferred materials, writing style, and common job scopes to produce proposals that sound like the contractor wrote them personally.

**Problem being solved:** Home service contractors lose jobs because their proposals look unprofessional, take too long to create, or never get sent at all. Most contractors estimate from memory, scribble numbers on paper, or use generic templates that don't reflect their brand. The result: lost revenue, inconsistent pricing, and hours wasted on admin work instead of billable jobs. A contractor who can send a sharp proposal within an hour of a site visit closes significantly more work than one who takes three days.

**Target market size:** There are approximately 3.7 million home service businesses in the United States. Focusing on businesses with 1-25 employees in the plumbing, electrical, HVAC, roofing, painting, and landscaping verticals, the addressable market is roughly 1.8 million businesses. At an average revenue per account of $150/month, the total addressable market is approximately $3.2 billion annually. The serviceable obtainable market for year one, targeting English-speaking US contractors in the top 50 metro areas, is roughly $48 million.

## Stack
- Next.js 15 (App Router) + TypeScript + Tailwind CSS v4
- Supabase (auth, database, storage)
- Stripe (subscriptions with 14-day trial)
- Deployed on Vercel

## Design System
- **Heading font**: ** Inter (Google Fonts) - clean, modern, highly readable (from Google Fonts)
- **Body font**: ** Inter (Google Fonts) - consistent, works at all sizes (from Google Fonts)
- **Primary color**: #1E3A5F
- **Secondary color**: #F5A623
- **Accent color**: #2ECC71
- **Aesthetic**: ** Clean, no-nonsense, and professional. Think "the best-looking invoice you've ever received." Generous white space, clear hierarchy, large tap targets for mobile use. The interface should feel like it was built for someone wearing work gloves - big buttons, clear labels, no tiny text. Cards and containers use subtle shadows instead of borders. The overall feel is "I trust this company with my business" rather than "look how trendy this app is."

## 2. Target Persona

**Primary Persona: "Mike the Contractor"**

- **Job title:** Owner/operator or field manager of a home service company
- **Business size:** 1-15 employees, doing $250K-$3M in annual revenue
- **Tech comfort:** Uses a smartphone daily, comfortable with texting and basic apps, but not a "tech person." Has tried software before and abandoned it because it was too complicated. Prefers things that just work.
- **Age range:** 30-55
- **Location:** Suburban and urban areas across the US

**Daily workflow and pain points:**
- Wakes up early, checks schedule, drives to job sites all day
- Takes notes on a clipboard or in the Notes app on their phone after walking a job
- Gets home at 6-7 PM exhausted, then has to sit down and write proposals
- Often puts off proposal writing for days, losing the urgency of the sale
- Pricing is inconsistent - sometimes too high, sometimes leaving money on the table
- Proposals look different every time, no consistent brand
- Loses track of which proposals were sent, opened, or accepted
- Spouse or office manager sometimes helps with paperwork but it's still a bottleneck

**Current tools they use:**
- Paper and pen / clipboard
- iPhone Notes app or voice memos
- Microsoft Word or Google Docs templates
- QuickBooks for invoicing (but not for proposals)
- Maybe Jobber, Housecall Pro, or ServiceTitan for scheduling
- Text messages and email to send quotes (often just a number, no formal proposal)

**What would make them switch:**
- Can create a proposal from their truck in 5 minutes using voice notes or quick text input
- Proposals look professional and match their brand without design skills
- Pricing suggestions based on their history and local market
- Homeowners can sign digitally right from their phone
- It actually saves them time on day one, not after weeks of setup

## 3. Core Features (MVP)

### Feature 1: AI Proposal Builder
**User story:** "As a home service contractor, I want to describe a job in plain language and have the AI generate a complete, professional proposal so that I can send it to the homeowner within minutes of leaving the site."

**Acceptance criteria:**
- User can input job details via text field (plain English description of the work)
- User can select their trade/service category (plumbing, electrical, HVAC, roofing, painting, landscaping, general)
- AI generates a structured proposal with: job summary, detailed scope of work, materials list, pricing breakdown, estimated timeline, and terms/conditions
- User can edit any section of the generated proposal before finalizing
- Generated proposal uses the contractor's saved business name, logo, and contact info
- **Priority: Must-have**

### Feature 2: Business Profile & Branding
**User story:** "As a contractor, I want to set up my company profile once so that every proposal automatically includes my logo, license number, and contact details."

**Acceptance criteria:**
- User can upload company logo (PNG, JPG, SVG)
- User can enter: business name, phone, email, address, license number, insurance info, website URL
- User can set default terms and conditions text
- User can choose a proposal color scheme from preset options
- Profile data auto-populates into every new proposal
- **Priority: Must-have**

### Feature 3: Proposal Templates Library
**User story:** "As a contractor, I want to save my best proposals as templates so that I can reuse them for similar jobs without starting from scratch."

**Acceptance criteria:**
- User can save any completed proposal as a named template
- Templates are organized by service category
- User can create a new proposal starting from any saved template
- System includes 5-10 pre-built starter templates per trade category
- Templates can be edited, duplicated, and deleted
- **Priority: Must-have**

### Feature 4: Customer Management
**User story:** "As a contractor, I want to keep track of my customers and their proposal history so that I can follow up and reference past work."

**Acceptance criteria:**
- User can create customer records with: name, email, phone, property address, notes
- Each customer shows a history of all proposals sent to them
- User can search and filter customers by name, address, or date
- Customer info auto-fills when creating a new proposal for an existing customer
- **Priority: Must-have**

### Feature 5: Proposal Sharing & E-Signature
**User story:** "As a contractor, I want to send proposals via email or shareable link and let homeowners sign digitally so that I can close deals faster without chasing paper."

**Acceptance criteria:**
- User can generate a unique shareable link for any proposal
- User can send the proposal directly via email from the platform
- Homeowners can view the proposal on any device without creating an account
- Homeowners can accept and e-sign the proposal with a typed signature and date
- Contractor receives a notification when a proposal is viewed, accepted, or declined
- Signed proposals generate a timestamped PDF record
- **Priority: Must-have**

### Feature 6: Proposal Dashboard & Tracking
**User story:** "As a contractor, I want to see all my proposals in one place with their status so that I know which ones need follow-up."

**Acceptance criteria:**
- Dashboard shows proposals organized by status: Draft, Sent, Viewed, Accepted, Declined, Expired
- Each proposal card shows: customer name, job title, amount, date, and current status
- User can filter by status, date range, and customer
- Dashboard shows summary stats: total proposals, acceptance rate, total value of accepted proposals
- **Priority: Must-have**

### Feature 7: Pricing History & Suggestions
**User story:** "As a contractor, I want the AI to suggest pricing based on my past proposals so that I price consistently and don't leave money on the table."

**Acceptance criteria:**
- AI analyzes the user's historical proposal data to suggest line item pricing
- Suggestions appear as hints when creating new proposals (user can accept or override)
- System tracks pricing trends over time per service category
- After 10+ proposals, pricing suggestions become noticeably more accurate
- **Priority: Nice-to-have (activates after enough data)**

### Feature 8: Photo Attachment
**User story:** "As a contractor, I want to attach job site photos to my proposals so that homeowners can see exactly what I'm referencing."

**Acceptance criteria:**
- User can upload up to 10 photos per proposal
- Photos can be reordered and captioned
- Photos appear in the shared proposal view
- Supports JPEG and PNG, max 10MB per image
- **Priority: Nice-to-have**

## 4. Data Model

### Entities and Fields

**users**
- id (UUID, PK)
- email (string, unique)
- password_hash (string, managed by Supabase Auth)
- created_at (timestamp)
- updated_at (timestamp)
- stripe_customer_id (string, nullable)
- subscription_tier (enum: free, starter, professional, business)
- subscription_status (enum: trialing, active, past_due, canceled)
- trial_ends_at (timestamp, nullable)
- monthly_proposal_count (integer, default 0)
- billing_period_start (timestamp)

**business_profiles**
- id (UUID, PK)
- user_id (UUID, FK -> users.id, unique)
- business_name (string)
- phone (string)
- email (string)
- address_line1 (string)
- address_line2 (string, nullable)
- city (string)
- state (string)
- zip (string)
- logo_url (string, nullable)
- license_number (string, nullable)
- insurance_info (text, nullable)
- website_url (string, nullable)
- default_terms (text, nullable)
- brand_color (string, default "#1E3A5F")
- trade_categories (string array)
- created_at (timestamp)
- updated_at (timestamp)

**customers**
- id (UUID, PK)
- user_id (UUID, FK -> users.id)
- first_name (string)
- last_name (string)
- email (string, nullable)
- phone (string, nullable)
- property_address_line1 (string)
- property_address_line2 (string, nullable)
- city (string)
- state (string)
- zip (string)
- notes (text, nullable)
- created_at (timestamp)
- updated_at (timestamp)

**proposals**
- id (UUID, PK)
- user_id (UUID, FK -> users.id)
- customer_id (UUID, FK -> customers.id, nullable)
- template_id (UUID, FK -> templates.id, nullable)
- title (string)
- status (enum: draft, sent, viewed, accepted, declined, expired)
- trade_category (string)
- job_description_input (text) -- the raw input from the contractor
- scope_of_work (text) -- AI-generated, editable
- materials_list (JSONB) -- array of {item, quantity, unit_price, total}
- labor_items (JSONB) -- array of {description, hours, rate, total}
- pricing_breakdown (JSONB) -- {subtotal, tax_rate, tax_amount, discount, total}
- total_amount (decimal)
- estimated_timeline (string)
- terms_and_conditions (text)
- notes_to_customer (text, nullable)
- valid_until (date, nullable)
- share_token (string, unique) -- for public sharing link
- sent_at (timestamp, nullable)
- viewed_at (timestamp, nullable)
- signed_at (timestamp, nullable)
- signature_data (JSONB, nullable) -- {name, signature_text, ip_address, timestamp}
- signed_pdf_url (string, nullable)
- created_at (timestamp)
- updated_at (timestamp)

**proposal_photos**
- id (UUID, PK)
- proposal_id (UUID, FK -> proposals.id)
- photo_url (string)
- caption (string, nullable)
- sort_order (integer)
- created_at (timestamp)

**templates**
- id (UUID, PK)
- user_id (UUID, FK -> users.id, nullable) -- null for system templates
- name (string)
- trade_category (string)
- is_system_template (boolean, default false)
- scope_of_work (text)
- materials_list (JSONB)
- labor_items (JSONB)
- terms_and_conditions (text, nullable)
- estimated_timeline (string, nullable)
- created_at (timestamp)
- updated_at (timestamp)

**ai_learning_data**
- id (UUID, PK)
- user_id (UUID, FK -> users.id)
- trade_category (string)
- job_type (string) -- e.g., "water heater replacement", "panel upgrade"
- pricing_data (JSONB) -- historical pricing for this job type
- preferred_materials (JSONB) -- materials this contractor typically uses
- writing_style_notes (JSONB) -- tone, common phrases, terminology
- proposal_count (integer) -- how many proposals contributed to this data
- created_at (timestamp)
- updated_at (timestamp)

**usage_records**
- id (UUID, PK)
- user_id (UUID, FK -> users.id)
- action_type (enum: proposal_generated, proposal_sent, ai_revision)
- proposal_id (UUID, FK -> proposals.id, nullable)
- stripe_reported (boolean, default false)
- created_at (timestamp)

### Relationships
- users 1:1 business_profiles
- users 1:many customers
- users 1:many proposals
- users 1:many templates
- users 1:many ai_learning_data
- users 1:many usage_records
- customers 1:many proposals
- proposals 1:many proposal_photos
- templates 1:many proposals (optional reference)

## 5. Pages & Routes

### Public Pages (no auth required)

**/ (Landing Page)**
- Hero section with headline, subheadline, and CTA button
- Problem/solution section showing the pain of manual proposals
- Feature showcase (3-4 key features with visuals)
- How it works (3-step process)
- Pricing table with three tiers
- Testimonials section (placeholder content for launch)
- FAQ section
- Final CTA section
- Footer with links to /terms, /privacy, /blog, /demo

**/login**
- Email and password login form
- "Forgot password" link
- Link to /signup

**/signup**
- Email and password registration form
- Trade category selection (multi-select)
- Business name field
- Fires n8n signup webhook on success
- Redirects to /dashboard/onboarding

**/demo**
- Interactive product tour with guided walkthrough
- Animated screenshots or embedded video showing: creating a proposal, AI generation, sending to customer, e-signature
- Sample proposal viewer (read-only example of a finished proposal)
- CTA buttons: "Start Free Trial" and "Book a Demo Call" (links to cal.com/shalinp)

**/blog**
- Blog listing page with post cards
- Individual blog post pages at /blog/[slug]

**/terms**
- Terms of service with binding arbitration clause, limitation of liability, AI disclaimer

**/privacy**
- Privacy policy

**/p/[share_token] (Public Proposal View)**
- No auth required
- Displays the full proposal with branding
- Shows photos if attached
- Accept/decline buttons
- E-signature capture (typed name, checkbox for agreement)
- Thank you confirmation after signing

### Authenticated Pages (auth required)

**/dashboard**
- Proposal summary stats (total, sent, accepted, acceptance rate, total revenue)
- Recent proposals list (last 10)
- Quick action buttons: "New Proposal", "View All Proposals"
- Notification area for proposal status changes

**/dashboard/onboarding**
- Step-by-step setup wizard: business info, logo upload, default terms, first template selection
- Shown on first login, skippable after

**/dashboard/proposals**
- Full proposal list with status filters
- Search by customer name or proposal title
- Sort by date, amount, status
- Pagination

**/dashboard/proposals/new**
- Job description text input (large textarea)
- Customer selection (existing or create new inline)
- Trade category selector
- Optional: start from template dropdown
- "Generate Proposal" button that triggers AI
- Loading state while AI processes

**/dashboard/proposals/[id]**
- Full proposal view and editor
- Editable sections: title, scope, materials, labor, timeline, terms, notes
- Photo upload area
- Pricing calculator (auto-updates total as line items change)
- Action buttons: Save Draft, Send to Customer, Download PDF, Save as Template
- Status indicator and history (sent, viewed, signed timestamps)

**/dashboard/proposals/[id]/preview**
- Read-only preview showing exactly what the customer will see
- Print-friendly layout

**/dashboard/customers**
- Customer list with search and sort
- Each row shows: name, phone, email, proposal count, total value

**/dashboard/customers/new**
- Customer creation form

**/dashboard/customers/[id]**
- Customer detail view with edit capability
- Proposal history for this customer

**/dashboard/templates**
- List of user templates and system templates
- Filter by trade category
- Create, edit, duplicate, delete actions

**/dashboard/templates/[id]**
- Template editor (same layout as proposal editor but without customer-specific fields)

**/dashboard/settings**
- Business profile editor
- Account settings (email, password change)
- Subscription management (current plan, usage stats, upgrade/downgrade)
- Link to Stripe billing portal
- Default proposal settings (expiration days, tax rate, payment terms)

**/dashboard/settings/billing**
- Current plan details
- Usage this billing period (proposals generated, proposals sent)
- Upgrade/downgrade options
- Stripe billing portal link for invoice history and payment method management

### Navigation Structure

**Public navigation (top bar):**
Features | Pricing | Blog | Demo | Login | Sign Up (CTA button)

**Authenticated navigation (sidebar):**
- Dashboard (home icon)
- Proposals (document icon)
  - All Proposals
  - New Proposal
- Customers (people icon)
- Templates (copy icon)
- Settings (gear icon)
  - Business Profile
  - Billing
  - Account

## 7. Pricing Tiers

### Tier 1: Starter - $79/month
- Up to 15 AI-generated proposals per month
- Business profile and branding
- Customer management (up to 50 customers)
- 5 custom templates
- Proposal sharing via link
- Email delivery
- E-signature capture
- PDF download
- Access to system templates
- Email support

### Tier 2: Professional - $149/month
- Up to 50 AI-generated proposals per month
- Everything in Starter, plus:
- Unlimited customers
- Unlimited custom templates
- AI pricing suggestions (learns from your history)
- Photo attachments (up to 10 per proposal)
- Proposal analytics (view tracking, time-to-sign)
- Priority email support
- Custom terms and conditions per proposal
- Bulk proposal actions

### Tier 3: Business - $249/month
- Unlimited AI-generated proposals
- Everything in Professional, plus:
- Team member accounts (up to 5 users)
- Role-based permissions (admin, estimator, viewer)
- Company-wide template library
- Advanced analytics and reporting
- API access for custom integrations
- White-label proposal URLs (coming soon)
- Phone support
- Dedicated onboarding call

**All tiers include:**
- 14-day free trial (no credit card required to start, card required to continue)
- Access to the core AI proposal generation engine
- Mobile-responsive interface

**Usage-based pricing (metered via Stripe):**
- Proposals beyond tier limits: $3.00 per additional AI-generated proposal
- Overage is tracked via Stripe usage records and billed at the end of each billing cycle
- Users receive a warning at 80% and 100% of their monthly limit

**Free tier (for viral growth):**
- 3 AI-generated proposals per month
- 1 custom template
- Up to 10 customers
- Basic proposal sharing (no e-signature)
- "Powered by ProposalPro" watermark on shared proposals
- Available indefinitely, no trial expiration

## 8. Required Integrations

### Supabase Auth
- Email + password authentication
- Password reset flow
- Session management
- Row Level Security (RLS) policies on all tables so users can only access their own data

### Stripe Checkout
- Three subscription products matching the pricing tiers (Starter $79, Professional $149, Business $249)
- Each product has a monthly recurring price
- 14-day free trial on all paid tiers
- Metered price component for overage proposals ($3.00 per unit)
- Usage records submitted via Stripe's usage_record API when a user generates a proposal beyond their tier limit
- Stripe Customer Portal for self-service billing management
- Checkout session created server-side with success/cancel URLs

### Webhooks (n8n)
- **Stripe events:** POST to ${NEXT_PUBLIC_N8N_URL}/webhook/stripe-events
  - Handles: checkout.session.completed, customer.subscription.updated, customer.subscription.deleted, invoice.payment_failed, invoice.paid
  - Updates user subscription_tier and subscription_status in Supabase
- **User signup:** POST to ${NEXT_PUBLIC_N8N_URL}/webhook/user-signup
  - Payload: {email, business_name, trade_categories, signup_date}
  - Triggers welcome email sequence
- **Support ticket:** POST to ${NEXT_PUBLIC_N8N_URL}/webhook/support-ticket
  - Payload: {name, email, subject, message, page_url, user_id (if authenticated)}

### Contact Form
- Available on landing page footer and /dashboard/settings
- Fields: name, email, subject, message
- Posts to ${NEXT_PUBLIC_N8N_URL}/webhook/support-ticket
- Shows confirmation message on submit

### /demo Route
- Interactive self-serve product tour
- Step-by-step walkthrough with annotated screenshots or animations:
  1. Entering job details
  2. AI generating a proposal
  3. Editing and customizing
  4. Sending to the homeowner
  5. Customer viewing and signing
- Sample read-only proposal that visitors can interact with
- CTA buttons: "Start Your Free Trial" (links to /signup) and "Book a Demo Call" (links to cal.com/shalinp)

### Plausible Analytics
- Script tag with data-domain from NEXT_PUBLIC_PLAUSIBLE_DOMAIN env var
- Loaded on all pages
- Custom events for: signup_completed, proposal_generated, proposal_sent, proposal_accepted, checkout_started

### Live Chat Widget
- Tawk.to free tier (or Crisp as fallback)
- Floating button in bottom-right corner on all pages
- Widget ID from NEXT_PUBLIC_TAWKTO_ID env var
- Messages route to ${NEXT_PUBLIC_N8N_URL}/webhook/support-ticket via Tawk.to webhook configuration
- Custom greeting: "Hey! Got questions about creating proposals? We're here to help."

### Environment Variables
```
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_ROLE_KEY=
NEXT_PUBLIC_N8N_URL=
NEXT_PUBLIC_PLAUSIBLE_DOMAIN=
NEXT_PUBLIC_TAWKTO_ID=
STRIPE_SECRET_KEY=
STRIPE_WEBHOOK_SECRET=
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=
STRIPE_STARTER_PRICE_ID=
STRIPE_PROFESSIONAL_PRICE_ID=
STRIPE_BUSINESS_PRICE_ID=
STRIPE_METERED_PRICE_ID=
OPENAI_API_KEY=
NEXT_PUBLIC_APP_URL=
```

## 9. SEO Plan

### Target Keywords (with estimated monthly search volume)

1. "proposal software for contractors" - 720/mo
2. "contractor estimate template" - 2,400/mo
3. "HVAC proposal template" - 880/mo
4. "plumbing estimate software" - 480/mo
5. "home service proposal generator" - 320/mo
6. "contractor bid software" - 590/mo
7. "roofing estimate template" - 1,100/mo
8. "how to write a contractor proposal" - 1,300/mo
9. "electrical estimate software" - 390/mo
10. "landscaping proposal template" - 720/mo

### Initial Blog Posts

1. **"How to Write a Winning Contractor Proposal (With Examples)"** - Targets "how to write a contractor proposal." Practical guide with real proposal examples for different trades.

2. **"The 7 Biggest Mistakes Contractors Make on Estimates (And How to Fix Them)"** - Targets "contractor estimate template" and related terms. Covers common pricing errors, missing details, and unprofessional formatting.

3. **"HVAC Proposal Template: What to Include and Why It Matters"** - Targets "HVAC proposal template." Includes a downloadable template and walkthrough of each section.

4. **"Why Contractors Who Send Proposals Within 24 Hours Win More Jobs"** - Targets "proposal software for contractors." Data-driven post about speed-to-proposal and close rates.

5. **"Roofing Estimate Template: A Complete Guide for Roofing Contractors"** - Targets "roofing estimate template." Detailed breakdown of what a roofing proposal should include, with material and labor line item examples.

### Landing Page Meta Tags

**Meta title:** "AI Proposal Generator for Contractors | Create Professional Proposals in Minutes"

**Meta description:** "Stop losing jobs to slow, ugly proposals. Our AI proposal generator helps home service contractors create professional, branded proposals in minutes. Try it free for 14 days."

### Structured Data (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "ProposalPro - AI Proposal Generator for Contractors",
  "applicationCategory": "BusinessApplication",
  "operatingSystem": "Web",
  "description": "AI-powered proposal generator for home service contractors. Create professional proposals in minutes.",
  "offers": {
    "@type": "AggregateOffer",
    "lowPrice": "79",
    "highPrice": "249",
    "priceCurrency": "USD",
    "offerCount": "3"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "ratingCount": "127"
  },
  "featureList": [
    "AI proposal generation",
    "E-signature capture",
    "Customer management",
    "Proposal tracking",
    "Custom branding",
    "PDF export"
  ]
}
```

## 10. Competitive Weaknesses to Exploit

Based on common complaints found in reviews of competing tools (Jobber, Housecall Pro, ServiceTitan, Joist, Bidsketch, PandaDoc):

### 1. "Too complicated - I just need to send proposals, not run NASA"
**Competitor issue:** Tools like ServiceTitan and Housecall Pro are full field service management platforms. Contractors who just want better proposals are forced to buy (and learn) an entire business suite.
**Our approach:** We do one thing and do it well. Proposal creation and delivery. No scheduling, no dispatching, no inventory management cluttering the interface. A contractor can sign up and send their first AI-generated proposal in under 10 minutes.

### 2. "Proposals look generic and templated"
**Competitor issue:** Many tools offer rigid templates that all look the same. Contractors complain their proposals look identical to every other company using the same software.
**Our approach:** AI generates unique, natural-sounding proposal text for each job. Combined with the contractor's branding (logo, colors, custom terms), every proposal feels custom-written rather than fill-in-the-blank.

### 3. "Pricing is insane for a small operation"
**Competitor issue:** ServiceTitan starts at $300+/month. Housecall Pro is $65+/month but requires add-ons for proposal features. Many tools charge per user, making it expensive for small teams.
**Our approach:** Starter plan at $79/month with everything a solo contractor needs. Free tier available for the smallest operators. No per-user charges until the Business tier, and even then it includes 5 users.

### 4. "Mobile experience is terrible"
**Competitor issue:** Many competitors were built desktop-first. Contractors in the field trying to create proposals on their phone deal with tiny buttons, broken layouts, and features that only work on desktop.
**Our approach:** Mobile-first design philosophy. Every feature works on a phone screen. Large touch targets, simplified mobile layouts, and the ability to generate a full proposal from a phone in the truck.

### 5. "Customer support is nonexistent"
**Competitor issue:** Multiple competitors have 1-star reviews specifically about slow or unhelpful support. Contractors can't afford to wait 3 days for a response when they're trying to close a job.
**Our approach:** Live chat on every page, support webhook that routes to our team immediately, and a /demo page that answers most questions before they're asked. Business tier includes phone support.

### 6. "No way to track if the customer even opened my proposal"
**Competitor issue:** Basic proposal tools send a PDF and that's it. The contractor has no idea if the homeowner looked at it, ignored it, or lost it.
**Our approach:** Built-in proposal tracking shows when a proposal was viewed, how long the customer spent on it, and whether they accepted or declined. Contractors get real-time notifications.

## Content Quality Standards (MANDATORY)
BANNED WORDS: "delve", "leverage", "utilize", "harness", "elevate", "empower", "streamline", "robust", "seamless", "cutting-edge", "game-changer", "revolutionize", "transform", "innovative", "best-in-class", "world-class", "state-of-the-art", "paradigm", "synergy", "holistic"
BANNED PUNCTUATION: em dashes (use regular dashes instead)
Write like a real person. Direct, practical, no BS. Conversational tone.

## Development Rules
- Always use App Router (app/ directory)
- Use TypeScript strict mode
- Use Tailwind CSS v4 for all styling
- Use Supabase client from @supabase/ssr
- All pages must be responsive (mobile-first)
- Use Server Components by default, Client Components only when needed
- Follow the design system defined above for ALL UI elements
- Include sitemap.xml and robots.txt
- Add JSON-LD structured data to landing page
- Include OG image meta tags on all pages
- Lighthouse targets: performance > 50, accessibility > 80, SEO > 80

## Legal Pages (MANDATORY)
Every app MUST include the following legal pages, accessible from the footer:

### /terms - Terms of Service
Must include ALL of the following provisions:
- **Binding Arbitration Clause**: All disputes shall be resolved through binding arbitration administered by the American Arbitration Association (AAA) under its Commercial Arbitration Rules, conducted in the State of Delaware. Users waive the right to a jury trial and to participate in class actions.
- **Class Action Waiver**: Users agree to resolve disputes individually and waive any right to bring or participate in class action lawsuits or class-wide arbitration.
- **Limitation of Liability**: Total liability capped at the amount paid by the user in the 12 months preceding the claim. No liability for indirect, incidental, special, consequential, or punitive damages.
- **Disclaimer of Warranties**: Service provided "AS IS" and "AS AVAILABLE" without warranties of any kind, express or implied, including merchantability, fitness for a particular purpose, and non-infringement.
- **AI-Generated Content Disclaimer**: Clearly state that portions of the service may use artificial intelligence and machine learning. AI outputs are provided for informational purposes only and should not be relied upon as professional advice. The company makes no guarantees about the accuracy, completeness, or reliability of AI-generated content.
- **Indemnification**: Users agree to indemnify and hold harmless the company, its officers, directors, employees, and agents from any claims arising from their use of the service.
- **Governing Law**: State of Delaware, United States.
- **Modification Rights**: Company reserves the right to modify terms at any time with notice. Continued use constitutes acceptance.
- **Termination**: Company may terminate or suspend access immediately, without prior notice, for any reason including breach of terms.
- **Severability**: If any provision is found unenforceable, remaining provisions continue in effect.
- **Acceptable Use**: Prohibit illegal use, reverse engineering, scraping, unauthorized access, and interference with the service.
- **Intellectual Property**: All content, features, and functionality are owned by the company and protected by copyright, trademark, and other IP laws.

### /privacy - Privacy Policy
Must include:
- What data is collected (account info, usage data, cookies, analytics)
- How data is used (service delivery, improvement, communication)
- Third-party services used (Supabase for database, Stripe for payments, Plausible for analytics)
- Data retention and deletion policies
- User rights (access, correction, deletion of personal data)
- Cookie policy
- Contact information for privacy inquiries
- CCPA/GDPR compliance language
- Children's privacy (not directed at under-13)
- Data security measures

### Footer Requirements
- Links to Terms of Service and Privacy Policy must appear in the site footer on every page
- Copyright notice: "© 2026 AI Proposal Generator for Home Service Contractors. All rights reserved."

### Legal Content Standards
- Write in plain, readable English - not dense legalese
- Use headers and sections for easy navigation
- Include "Last Updated" date at the top
- Make it clear this is a binding legal agreement

## Environment Variables (.env.example)
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_ROLE_KEY=
STRIPE_SECRET_KEY=
STRIPE_WEBHOOK_SECRET=
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=
NEXT_PUBLIC_N8N_URL=
NEXT_PUBLIC_PLAUSIBLE_DOMAIN=
NEXT_PUBLIC_SITE_URL=
