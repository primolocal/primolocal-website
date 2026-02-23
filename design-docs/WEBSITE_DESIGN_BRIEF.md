# PRIMOLOCAL WEBSITE — DESIGN BRIEF
## Professional Web Design Project Specification

**Client:** PrimoLocal  
**Project:** Complete website redesign (No-Sales-Call Model)  
**Platform:** Netlify (static site)  
**Domain:** primolocal.org  
**Target Launch:** March 1, 2026  
**Budget:** [To be determined]  
**Designer:** [Your Name/Agency]

---

## 1. PROJECT OVERVIEW

### The Business
PrimoLocal provides 24/7 AI phone answering for local service businesses (plumbers, HVAC, roofers). The AI agent "CORA" answers calls, books appointments, and captures leads while business owners sleep or work.

### The Shift (CRITICAL)
**OLD MODEL:** Book sales calls → Qualify → Demo → Close (high friction)  
**NEW MODEL:** Drive to demo → Demo sells itself → Direct checkout (zero friction)

### The Goal
Website becomes a **demo generation machine**. Every element drives visitors to call 832-737-0525 and test CORA. No sales calls. No contact forms. Direct purchase path.

### Success Metrics
- 30+ demo calls per day from website
- 20%+ conversion on Founders page
- <2 second load time
- 60%+ mobile traffic optimized

---

## 2. TECHNICAL SPECIFICATIONS

### Platform & Hosting
- **Platform:** Static HTML/CSS/JS (no CMS needed)
- **Hosting:** Netlify (free tier)
- **Domain:** primolocal.org (client will configure DNS)
- **SSL:** Auto-provisioned via Netlify
- **CDN:** Netlify's global CDN

### Performance Requirements
- **Load Time:** <2 seconds (Lighthouse score 90+)
- **Mobile-First:** 60%+ traffic is mobile
- **Responsive:** All breakpoints (320px - 1920px+)
- **SEO:** Semantic HTML, meta tags, structured data
- **Accessibility:** WCAG 2.1 AA compliant

### Third-Party Integrations
1. **Stripe Payment Links** (checkout on /founders)
   - Founders: https://buy.stripe.com/[FOUNDERS_LINK]
   - Annual: https://buy.stripe.com/[ANNUAL_LINK]
   - Monthly: https://buy.stripe.com/[MONTHLY_LINK]

2. **Analytics**
   - Google Analytics 4
   - Google Tag Manager
   - Hotjar (heatmaps)

3. **Click-to-Call**
   - All phone numbers: `tel:8327370525`
   - Sticky mobile CTA

4. **Live Counter (JavaScript)**
   - Display: "17 of 20 Founders spots taken"
   - Update via simple JSON/API or static with manual updates

### File Structure
```
/
├── index.html              (Homepage)
├── founders.html           (/founders — Offer Dock)
├── demo.html              (/demo)
├── about.html             (/about)
├── results.html           (/results)
├── resources.html         (/resources)
├── css/
│   ├── reset.css
│   ├── variables.css
│   ├── components.css
│   ├── pages.css
│   └── responsive.css
├── js/
│   ├── main.js
│   ├── counter.js         (Founders spot counter)
│   ├── calculator.js      (ROI calculator)
│   └── analytics.js
├── images/
│   ├── logo.svg
│   ├── cora-interface.png
│   ├── testimonials/
│   └── icons/
├── audio/
│   └── cora-demo.mp3      (30-45 second demo call)
└── _redirects             (Netlify redirects file)
```

---

## 3. DESIGN SYSTEM

### Brand Identity
- **Brand Name:** PrimoLocal
- **Tagline:** "Never Miss a Call. Wake Up to Booked Appointments."
- **Personality:** Professional but approachable, trustworthy, innovative but grounded

### Logo
**Primary Logo:**
- **Icon:** Blue (#014FA4) circular location pin with "P" monogram inside
- **Wordmark:** "PrimoLocal" in Blue (#014FA4), modern sans-serif font
- **Accent:** Orange (#FFA269) may be used for emphasis/accents
- **Usage:** Icon + wordmark on headers, icon only for favicon/social
- **Files Needed:** SVG (primary), PNG (fallback), favicon.ico

**Logo Variations:**
- **Full color:** Blue icon + Blue text (primary) — per brand guidelines
- **White version:** White icon + text (for dark backgrounds)
- **Icon only:** Blue "P" pin (for favicon, social avatars)
- **Minimum size:** 120px width (full), 32px (icon only)

**Brand Colors (from Brand Guide):**
- **Primary Blue:** #014FA4 (Royal Blue)
- **Secondary Orange:** #FFA269 (Vibrant Orange)
- **Dark Slate:** #2D3748 (body text)
- **White:** #FFFFFF (backgrounds)

### Color Palette

**Primary Colors (from Brand Guide):**
- **Primary Blue:** #014FA4 (Royal Blue) — headers, buttons, trust elements
- **Primary Dark:** #013A7A (darker blue) — hover states
- **Primary Light:** #3B82F6 (lighter blue) — highlights, links

**Secondary Colors (from Brand Guide):**
- **Secondary Orange:** #FFA269 (Vibrant Orange) — CTAs, accents, urgency
- **Accent Orange:** #F97316 — badges, urgency highlights

**Semantic Colors:**
- **Success:** #2F855A (Forest Green) — savings, positive metrics, checkmarks
- **Urgency:** #C53030 (Emergency Red) — urgent warnings (sparingly)
- **Text Primary:** #2D3748 (Dark Slate) — headings
- **Text Secondary:** #4A5568 (slate) — body text
- **Background:** #FFFFFF (white)
- **Background Alt:** #F7FAFC (light gray sections)

**Gradient Combinations:**
- Hero: `linear-gradient(135deg, #F7FAFC 0%, #FFFFFF 100%)`
- CTA Sections: `linear-gradient(135deg, #014FA4 0%, #2563EB 100%)`
- Founders Card: `linear-gradient(135deg, #014FA4 0%, #3B82F6 100%)`
- Orange accents: `#FFA269` on blue backgrounds for maximum impact

### Typography

**Font Family:**
- **Primary:** 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif
- **Load from:** Google Fonts (https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap)

**Type Scale:**
- **H1:** 64px / 700 weight / line-height 1.1
- **H2:** 48px / 700 weight / line-height 1.2
- **H3:** 32px / 700 weight / line-height 1.3
- **H4:** 24px / 600 weight / line-height 1.4
- **Body Large:** 20px / 400 weight / line-height 1.6
- **Body:** 16px / 400 weight / line-height 1.6
- **Small:** 14px / 400 weight / line-height 1.5

**Responsive Typography:**
- H1: `clamp(2.5rem, 5vw, 4rem)`
- H2: `clamp(2rem, 4vw, 3rem)`

### Spacing System

**Section Padding:**
- XLarge: 120px vertical
- Large: 80px vertical
- Medium: 64px vertical
- Small: 48px vertical

**Container:**
- Max-width: 1200px
- Padding: 24px horizontal (16px on mobile)

**Component Spacing:**
- Grid gap: 32px
- Card padding: 32px
- Button padding: 16px 32px

### Border Radius
- Small: 4px
- Default: 8px
- Medium: 12px
- Large: 16px
- XL: 24px
- Full: 9999px (pills)

### Shadows
- Small: `0 1px 2px 0 rgba(0, 0, 0, 0.05)`
- Default: `0 1px 3px 0 rgba(0, 0, 0, 0.1)`
- Medium: `0 4px 6px -1px rgba(0, 0, 0, 0.1)`
- Large: `0 10px 15px -3px rgba(0, 0, 0, 0.1)`

---

## 4. COMPONENT LIBRARY

### Buttons

**Primary Button (CTA):**
- Background: #2563eb
- Text: White, 16px, 600 weight
- Padding: 16px 32px
- Border-radius: 8px
- Hover: #1d4ed8, transform: translateY(-2px)
- Box-shadow on hover

**Secondary Button:**
- Background: transparent
- Border: 2px solid #2563eb
- Text: #2563eb
- Hover: Background #eff6ff

**Phone Button (Sticky):**
- Background: #10b981 (green)
- Icon: Phone icon left
- Text: "Call 832-737-0525"
- Border-radius: 9999px (pill)
- Sticky bottom on mobile

**Founders Button (Special):**
- Background: Gradient (#2563eb to #7c3aed)
- Text: White, bold
- Pulse animation (subtle)
- Size: Large (20px padding)

### Cards

**Pricing Card:**
- Background: White
- Border: 1px solid #e5e7eb
- Border-radius: 16px
- Padding: 32px
- Shadow: Medium
- Hover: Shadow large, translateY(-4px)

**Founders Card (Highlighted):**
- Background: Gradient border effect
- Border: 2px solid #f59e0b
- Badge: "BEST VALUE — 3 LEFT"
- Shadow: Large
- Scale: 1.05 (slightly larger)

**Testimonial Card:**
- Background: White
- Border-radius: 12px
- Quote marks: Large, light gray
- Avatar: 64px circle
- Name + Title + Result metrics

### Forms
**Note:** Minimal forms. Only on checkout (Stripe handles it).

### Icons
- **Library:** Lucide or Heroicons
- **Style:** Outline, 24px default
- **Usage:** Phone, Calendar, Check, Star, Shield, Clock

---

## 5. PAGE SPECIFICATIONS

---

### PAGE 1: HOMEPAGE (index.html)
**Primary Goal:** Drive demo calls to 832-737-0525

#### Section 1: Hero
**Layout:** Full-width, centered content, gradient background

**Content:**
- **Badge:** "🎯 17 Local Businesses Trust CORA"
- **Headline:** "Never Miss a Call. Wake Up to Booked Appointments."
- **Subheadline:** "CORA answers your business calls 24/7 — while you sleep, while you're on jobs, while you're with your family. One emergency job per week pays for the entire year."
- **Primary CTA Button:** "📞 TEST CORA NOW — CALL 832-737-0525"
  - Subtext: "Press 2 for demo. Takes 60 seconds."
- **Secondary CTA Link:** "Lock in Founders Pricing →"

**Trust Bar (below fold):**
- ⭐⭐⭐⭐⭐ "Booked 12 after-hours jobs in my first month" — Mike J.
- 🏆 17 Local Businesses Trust CORA
- 🎯 30-Day "Show Me The Jobs" Guarantee

**Visual:**
- Background: Subtle gradient (gray to white)
- Illustration: Phone showing CORA interface OR
- Abstract wave/sound visualization

**Animation:**
- CTA button: Subtle pulse
- Trust badges: Fade in stagger

#### Section 2: The Math (Cost of Missed Calls)
**Layout:** Two-column (text left, visual right on desktop)

**Content:**
- **Eyebrow:** "THE $40,000 QUESTION"
- **Headline:** "What Happens to Calls When You're On a Job?"
- **Copy:**
  - One emergency job = $800-1,500
  - Miss one per week = $40-75K per year
  - Where do those customers go? To your competitor.
- **Visual:** Simple calculator or chart showing revenue loss
- **CTA:** "See what you're losing. Test CORA: 832-737-0525"

#### Section 3: How It Works
**Layout:** Three columns (steps)

**Content:**
- **Eyebrow:** "3 STEPS TO NEVER MISS ANOTHER CALL"
- **Headline:** "Setup in 48 Hours. Work for Years."

**Step 1:**
- **Icon:** Chat/Discovery
- **Title:** "Discovery (15 min)"
- **Text:** "We learn your services, area, and how you want calls handled."

**Step 2:**
- **Icon:** Settings/Setup
- **Title:** "Setup (24-48 hrs)"
- **Text:** "We train CORA on your business and integrate your calendar."

**Step 3:**
- **Icon:** Check/Complete
- **Title:** "Go Live"
- **Text:** "Forward your number. CORA answers. You book jobs."

**CTA:** "Ready? Test CORA now: 832-737-0525"

#### Section 4: Meet CORA (Audio Demo)
**Layout:** Centered, audio player prominent

**Content:**
- **Headline:** "Hear CORA in Action"
- **Subheadline:** "Real demo call. 45 seconds."

**Audio Player:**
- Custom styled HTML5 audio player
- Play button prominent
- Waveform visualization (optional)
- Transcript expandable below

**Sample Transcript Preview:**
> "Hi, this is CORA with [Your Business]. I understand you have an emergency. Let me get someone out to you quickly..."

**CTA:** "Test CORA yourself: 832-737-0525"

#### Section 5: Social Proof
**Layout:** Three testimonial cards

**Content:**
- **Eyebrow:** "TRUSTED BY PLUMBERS, HVAC, AND ROOFERS"
- **Headline:** "Real Results from Real Businesses"

**Testimonial 1:**
- Quote: "I was skeptical. I called the demo and tried to break it. Couldn't tell it was AI. Signed up that day."
- Name: Mike J., Houston Plumber
- Result: "📈 12 after-hours jobs in month 1"
- Avatar: [Placeholder for photo]

**Testimonial 2:**
- Quote: "My wife was ready to leave me. 70-hour weeks answering calls. CORA gave me my Sundays back."
- Name: Robert K., HVAC Tech
- Result: "📈 Booked $18K in emergency calls first month"

**Testimonial 3:**
- Quote: "One $2,800 emergency job paid for 6 months of CORA. Wish I'd found this sooner."
- Name: Dave S., Roofing Contractor
- Result: "📈 3x ROI in 30 days"

#### Section 6: The Guarantee
**Layout:** Centered, prominent box

**Content:**
- **Icon:** Shield
- **Headline:** "30-Day 'Show Me The Jobs' Guarantee"
- **Copy:** "If CORA doesn't book you at least one paying job in your first 30 days, you pay nothing. Full refund, no questions, no hard feelings."
- **Subtext:** "We're that confident."

#### Section 7: Pricing Preview
**Layout:** Three pricing cards (Monthly, Annual, Founders)

**Content:**
- **Eyebrow:** "SIMPLE, TRANSPARENT PRICING"
- **Headline:** "Choose What Works for You"

**Card 1 — Monthly:**
- Price: "$497/month"
- Setup: "+ $497 setup"
- Features: [Bullet list]
- CTA: "Select Monthly"

**Card 2 — Annual:**
- Price: "$4,970/year"
- Savings: "Save $1,000+"
- Setup: "Waived"
- CTA: "Select Annual"

**Card 3 — Founders (Highlighted):**
- Badge: "BEST VALUE"
- Price: "$4,473/year"
- Savings: "Save $1,500+"
- Setup: "Waived"
- Extra: "Rate locked forever"
- Counter: "17 of 20 spots"
- CTA: "Lock in Founders →"

**Note:** These link to /founders page for full checkout

#### Section 8: Final CTA
**Layout:** Full-width, gradient background

**Content:**
- **Headline:** "Stop Losing Customers to Voicemail"
- **Copy:** "Your competitors are answering at 8 PM. They're booking the emergency calls you're missing. Test CORA in 60 seconds. If you're impressed, lock in your Founders spot. If not, no hard feelings."
- **Primary CTA:** "📞 CALL 832-737-0525 — TEST DEMO NOW"
- **Secondary CTA:** "Lock in Founders Pricing →"
- **Trust Bar:** 30-day guarantee | 17/20 Founders spots | Setup in 24-48 hours

---

### PAGE 2: FOUNDERS PAGE (/founders)
**Primary Goal:** Direct purchase of Founders plan
**Note:** Minimize distractions. Focus on conversion.

#### Header (Simple)
- Logo left
- Phone number right: "Questions? 832-737-0525"
- NO navigation menu (reduces exit clicks)

#### Section 1: Promise
**Content:**
- **Logo:** PrimoLocal
- **Headline:** "Never Miss a Call. Wake Up to Booked Appointments."
- **Subheadline:** "CORA answers your business calls 24/7 — while you sleep, while you're on jobs, while you're with your family."

#### Section 2: The Guarantee (Prominent)
**Layout:** Large highlighted box

**Content:**
- 🛡️ **30-Day "Show Me The Jobs" Guarantee**
- "If CORA doesn't book you at least one paying job in your first 30 days, you pay nothing. Full refund, no questions."
- "We're that confident."

#### Section 3: What's Included
**Layout:** Checklist, two columns

**Content:**
- ✅ 24/7 Professional Answering (real-sounding AI)
- ✅ Custom Script (trained on your business)
- ✅ Calendar Integration (books directly)
- ✅ SMS Notifications (instant alerts)
- ✅ Bilingual Support (English + Spanish)
- ✅ Monthly Reports (analytics + optimization)
- ✅ Setup in 24-48 Hours (we handle everything)
- ✅ Direct Founder Access (cell + WhatsApp)
- ✅ Quarterly Strategy Calls

#### Section 4: Pricing Tiers
**Layout:** Three cards, Founders highlighted

**Card 1 — Monthly:**
- Price: "$497/month"
- Setup: "+ $497"
- Best for: "Testing the waters"
- CTA: Stripe link for Monthly

**Card 2 — Annual:**
- Price: "$4,970/year"
- Savings: "Save $1,000+"
- Setup: "Waived"
- CTA: Stripe link for Annual

**Card 3 — Founders (Highlighted):**
- Badge: "BEST VALUE — ONLY 3 LEFT"
- Price: "$4,473/year"
- Savings: "$1,500+ vs monthly"
- Setup: "Waived ($497 value)"
- Extra perks list
- **Primary CTA:** "LOCK IN FOUNDERS →" (Stripe link)

**Live Counter:**
- "🔥 17 of 20 Founders spots taken"
- JavaScript counter with animation
- Subtext: "Once we hit 20, Founders closes forever."

#### Section 5: Trust
**Layout:** Testimonial + trust badges

**Content:**
- Quote: "Locked in Founders in January. Already captured 8 emergency calls that would've gone to my competitor. CORA paid for itself in 2 weeks." — James T.
- Badges: ⭐⭐⭐⭐⭐ | 🔒 SSL Secure | 💳 Stripe | 🛡️ 30-Day Guarantee

#### Section 6: FAQ
**Layout:** Expandable accordion

**Questions:**
1. Will customers know it's AI?
2. What if CORA books something wrong?
3. Do I need a new phone number?
4. How fast can I get set up?
5. What if it doesn't work for my business?
6. Can I upgrade later?
7. What industries do you serve?

*(Copy provided in full content doc)*

#### Section 7: Final CTA
**Content:**
- **Headline:** "Join 17 Founders. Lock in your rate forever."
- **Copy:** "One emergency job per week = $40K+ per year. Founders rate: $4,473/year (never increases). Regular rate: $497/month ($5,964/year). You save $1,500+ every year. Forever."
- **CTA Button:** "LOCK IN FOUNDERS PRICING — $4,473/YEAR →"
- **Secondary:** "Questions? Text Tommy: 832-737-0525"

**Footer (Simple):**
- © 2026 PrimoLocal
- Text/call: 832-737-0525
- 30-day guarantee | Privacy | Terms

---

### PAGE 3: TEST CORA (/demo)
**Purpose:** Set expectations, then drive to call

#### Section 1: Instructions
**Content:**
- **Headline:** "Test CORA in 60 Seconds"
- **Subheadline:** "No signup. No credit card. Just call and see what happens."

**Steps:**
1. **Call 832-737-0525**
2. **Press 2 for Demo Mode**
3. **Pretend you're a customer with an emergency**
4. **Try to stump CORA**

**What to Ask (Examples):**
- "I have a burst pipe"
- "How much do you charge?"
- "Can you come right now?"
- "Do you service [your area]?"

**What You'll Experience:**
- CORA answers as your business
- She'll gather info and book an appointment
- You'll get a text confirmation
- Real-time scheduling

#### Section 2: Call CTA
**Layout:** Prominent box

**Content:**
- 📞 **Ready to Test?**
- **Call 832-737-0525**
- Press 2 for Demo
- *Takes 60 seconds. If you're not impressed, hang up.*
- **Button:** "Call Now" (tel: link)

#### Section 3: After the Demo
**Layout:** Three options

**Impressed?**
- "Great! Ready to lock it in?"
- **CTA:** "LOCK IN FOUNDERS →"
- "Only 3 spots left at $4,473/year"

**Have Questions?**
- "Text Tommy: 832-737-0525"
- "Don't worry — no sales pitch. Just answers."

**Not Ready?**
- "No problem. The demo line is always open: 832-737-0525"
- "Come back when you're ready."

---

### PAGE 4: ABOUT (/about)
**Purpose:** Story, mission, humanize the brand

#### Section 1: Story
**Content:**
- **Headline:** "Why I Built CORA"
- **Copy:** Personal story about Mike the plumber, 70-hour weeks, missing family time, building solution
- **Signature:** "— Tommy Premeaux, Founder"

#### Section 2: Mission
**Content:**
- **Headline:** "Our Mission"
- **Copy:** "Help local service businesses capture every opportunity without burning out."

#### Section 3: The Team
**Content:**
- **Tommy Premeaux** — Founder
- **CORA** — 24/7 AI Receptionist

#### Section 4: Contact
**Content:**
- **Fastest:** Text 832-737-0525
- **Email:** tommy@primolocal.org

---

### PAGE 5: RESULTS (/results)
**Purpose:** Case studies, proof, ROI

#### Section 1: Case Study (Mike)
**Content:**
- **Before:** Missing calls, 70-hour weeks, family stress
- **After:** 12 after-hours jobs, $14,400 revenue, normal hours
- **ROI:** 3.2x in first month
- **Quote:** "CORA gave me my life back."

#### Section 2: ROI Calculator
**Layout:** Interactive calculator

**Inputs:**
- Average Job Value: $[____]
- Missed Calls Per Week: [____]
- CORA Cost: $4,473/year

**Output:**
- "You're losing $[____]/year"
- "CORA pays for itself in [____] weeks"

**CTA:** "Calculate My ROI →" / "Test CORA: 832-737-0525"

---

### PAGE 6: RESOURCES (/resources)
**Purpose:** Content, FAQ, SEO

#### Section 1: Blog Posts (3-4 featured)
- "The $40K Cost of Voicemail"
- "How to Capture After-Hours Emergency Calls"
- "Old Way vs New Way"
- "From 70-Hour Weeks to Family Time"

#### Section 2: FAQ
- Expandable accordion
- Same questions as /founders page

#### Section 3: Setup Guide
- Step-by-step onboarding
- What to expect

#### Section 4: Contact
- Text: 832-737-0525
- Email: tommy@primolocal.org

---

## 6. GLOBAL ELEMENTS

### Navigation
**Header (All Pages):**
- **Logo:** PrimoLocal (left)
- **Nav Links:** Test CORA | Founders | Results | About
- **CTA Button:** "Call 832-737-0525" (right, always visible)

**Mobile:**
- Hamburger menu
- Sticky CTA bar at bottom: "📞 Call 832-737-0525"

**Footer (All Pages):**
- Quick Links: Test CORA | Lock in Founders | Results | About
- Contact: 832-737-0525 | tommy@primolocal.org
- Legal: Privacy | Terms | Guarantee
- © 2026 PrimoLocal

### Exit Intent Popup
**Trigger:** Mouse leaves viewport (desktop)

**Content:**
- "Before you go..."
- "Test CORA in 60 seconds. Call 832-737-0525, press 2 for demo."
- "If you're impressed, lock in Founders pricing. If not, no hard feelings."
- **Buttons:** [CALL NOW] [NO THANKS]

---

## 7. CONTENT DELIVERABLES

### Provided by Client
- [x] **Logo:** Red location pin "P" icon + "PrimoLocal" wordmark (provide SVG, PNG, favicon)
- [ ] Founder photo (Tommy)
- [ ] Testimonial photos (3 clients)
- [ ] CORA demo audio file (MP3, 30-45 seconds)
- [ ] Stripe Payment Links (3 URLs)
- [ ] Google Analytics ID
- [ ] Hotjar ID

### To Be Created
- [ ] All copy (provided in this document)
- [ ] Icons (Lucide or Heroicons)
- [ ] Custom graphics (calculator, phone mockups)

---

## 8. SEO REQUIREMENTS

### Meta Tags (All Pages)

**Homepage:**
- Title: "PrimoLocal — 24/7 AI Answering for Plumbers & HVAC"
- Description: "Never miss a call. CORA answers 24/7 and books appointments while you sleep. 30-day guarantee. Test the demo: 832-737-0525"

**Founders:**
- Title: "Founders Pricing — Lock in $4,473/Year | PrimoLocal"
- Description: "Join 17 Founders. Rate locked forever. 30-day guarantee. Only 3 spots left."

**Demo:**
- Title: "Test CORA — Free 60-Second Demo | PrimoLocal"
- Description: "Call 832-737-0525, press 2. See how CORA books appointments 24/7."

### Structured Data
- Organization schema
- Product schema (for pricing)
- FAQ schema (for FAQ sections)

### URL Structure
- Canonical URLs
- No trailing slashes
- 301 redirects if needed

---

## 9. ANALYTICS & TRACKING

### Events to Track
- Demo call initiated (tel: link click)
- Founders page view
- Pricing card clicks
- Checkout initiated (Stripe link click)
- FAQ expand
- Audio play
- ROI calculator use
- Exit intent shown

### Conversion Goals
- Demo calls (primary)
- Founders page visits
- Checkout completions

---

## 10. DELIVERABLES

### From Designer
1. **Design Files:** Figma or Adobe XD
2. **Style Guide:** Colors, typography, components
3. **Static Website:** HTML/CSS/JS files
4. **Assets:** Optimized images, icons, audio
5. **Documentation:** Component usage, update instructions

### File Handoff
- GitHub repository with all files
- README with setup instructions
- Netlify deployment guide

---

## 11. TIMELINE

### Week 1: Design
- Day 1-2: Homepage design
- Day 3: Founders page design
- Day 4: Remaining pages design
- Day 5: Mobile designs, design review

### Week 2: Development
- Day 1-2: HTML/CSS structure
- Day 3: JavaScript functionality
- Day 4: Responsive implementation
- Day 5: Content integration, testing

### Week 3: Testing & Launch
- Day 1: Cross-browser testing
- Day 2: Mobile testing
- Day 3: Performance optimization
- Day 4: Client review, revisions
- Day 5: Deploy to Netlify, go live

---

## 12. ACCEPTANCE CRITERIA

### Functionality
- [ ] All pages load correctly
- [ ] All CTAs work (tel: links, Stripe links)
- [ ] Mobile responsive (test on iOS/Android)
- [ ] Audio player works
- [ ] Live counter displays correctly
- [ ] ROI calculator functions
- [ ] Analytics events firing

### Performance
- [ ] Lighthouse score 90+
- [ ] Load time <2 seconds
- [ ] Images optimized
- [ ] CSS/JS minified

### Design
- [ ] Matches approved mockups
- [ ] Consistent styling across pages
- [ ] Accessibility compliant (WCAG 2.1 AA)
- [ ] Print styles (if applicable)

---

## 13. NOTES FOR DESIGNER

### Critical Success Factors
1. **Speed:** This site must load instantly. Optimize everything.
2. **Mobile:** 60%+ traffic is mobile. Design mobile-first.
3. **Clarity:** Every element drives to one action: Call 832-737-0525
4. **Trust:** Guarantee, testimonials, and transparency are essential
5. **Urgency:** The Founders scarcity is real. Make it visible but not aggressive

### What to Avoid
- ❌ Contact forms (we don't use them)
- ❌ "Book a Call" CTAs (replaced with demo call)
- ❌ Complex navigation (keep it simple)
- ❌ Stock photos (use real testimonial photos when possible)
- ❌ Slow load times (optimize ruthlessly)

### Brand Voice
- **Direct:** No fluff, no jargon
- **Confident:** We know this works
- **Helpful:** We're here to solve a problem
- **Honest:** Transparent pricing, real guarantee

---

## 14. CONTACT

**Client:** Tommy Premeaux  
**Email:** tommy@primolocal.org  
**Phone:** 832-737-0525  
**Domain:** primolocal.org (DNS to be configured)

**Stripe Account:** To be connected  
**Analytics Accounts:** To be provided

---

**Ready to start:** [Date]  
**Target completion:** [Date + 3 weeks]  
**Launch date:** March 1, 2026

---

*Professional Design Brief: PrimoLocal Website*  
*No-Sales-Call Model | Netlify Platform*
