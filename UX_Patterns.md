# UX Pattern Library — Evidence-Based Design Patterns
**Version:** 1.0 | **Scope:** Universal — all product types
**Complement to:** UIUX_Combined_for_Gem.md (UI visual patterns)
**This file covers:** User behavior, interaction flows, cognitive psychology, and UX strategy

---

## HOW TO USE THIS FILE

Each pattern entry contains:
- **What it is** — Definition
- **When to use** — Context and trigger conditions
- **Real-world examples** — Products that use it well
- **Psychology mechanism** — Why it works cognitively/behaviorally
- **Implementation checklist** — Actionable steps
- **Failure modes** — When it backfires
- **Success metrics** — How to measure effectiveness

---

# SECTION 1: ONBOARDING PATTERNS

---

## Pattern 1.1 — Progressive Onboarding

**What it is:**
Reveal features and complexity gradually, only when users need them. Don't teach everything upfront.

**When to use:**
- Products with 3+ core features
- Any tool where learning curve is a churn risk
- When user research shows >30% abandon during setup

**Real-world examples:**
- **Slack**: First shows only one channel, introduces features as user needs them
- **Notion**: Empty page with subtle hints; reveals template gallery only after first creation
- **Figma**: Starter file with annotations built-in teaching the tool as you use it
- **Linear**: No onboarding tour — you start with a demo workspace and learn by doing

**Psychology mechanism:**
- Cognitive Load Theory: Reduces intrinsic + extraneous load at first contact
- Competence reinforcement (Self-Determination Theory): Early quick wins build confidence
- Zeigarnik Effect: Incomplete tasks stay in memory — partial progress motivates continuation

**Implementation checklist:**
- [ ] Identify the "Aha Moment" — the single action that makes users understand the product's value
- [ ] Strip the first session to ONLY actions needed to reach Aha Moment
- [ ] Hide advanced features behind secondary navigation or "Pro" sections
- [ ] Use contextual tooltips triggered by user actions, not time
- [ ] Build an empty state that teaches, not just notifies

**Failure modes:**
- Hiding too much → users don't discover key features, feel product is limited
- Revealing too fast → overwhelm, same as no progressive onboarding
- No clear path to Aha Moment → users wander and churn

**Success metrics:**
- Time-to-Aha-Moment (lower is better)
- D1 Retention (users who return next day after signup)
- Feature discovery rate at Day 7 vs Day 1

---

## Pattern 1.2 — Social Proof Onboarding

**What it is:**
Use existing user success as the primary motivator during onboarding, not feature lists.

**When to use:**
- Marketplaces, creator platforms, social products
- Any product where "others are succeeding here" is a motivator
- When user psychology involves FOMO or social comparison

**Real-world examples:**
- **Airbnb**: "Hosts in [your city] earn $X/month on average" during host signup
- **Notion**: "Join 30 million people who organize their work with Notion"
- **Superhuman**: Waitlist + testimonials from known people before access
- **Coinbase**: Real-time trading volume displayed during account creation

**Psychology mechanism:**
- Social Proof (Cialdini): Uncertainty → look at others' behavior
- FOMO: Seeing others succeed creates urgency to participate
- In-group identity: "People like me" use this → I should too

**Implementation checklist:**
- [ ] Show real number of users/customers (specific beats vague)
- [ ] Include testimonials from users similar to the new user's profile
- [ ] Show success metrics of existing users at the relevant onboarding step
- [ ] Use localized proof when possible ("in Vietnam", "in your industry")
- [ ] Display activity indicators ("23 people signed up today")

**Failure modes:**
- Fake or unverifiable numbers destroy trust
- Generic testimonials from CEOs don't resonate with regular users
- Too many testimonials → choice paralysis and distrust

**Success metrics:**
- Signup completion rate
- Trust NPS at onboarding end
- Time-to-first-action post-signup

---

## Pattern 1.3 — Empty State as Teacher

**What it is:**
When a screen has no data yet, use that moment to teach the next action — not just display a blank screen.

**When to use:**
- Every list screen, dashboard, or feed screen
- New user's first session
- After user deletes all items

**Real-world examples:**
- **Linear**: Empty issue list shows keyboard shortcut to create first issue
- **Notion**: Blank page shows "/" command hint and template gallery
- **Airbnb**: Empty saved list shows "Start exploring" with curated options
- **Superhuman**: Empty inbox shows "You're at Inbox Zero" with celebration
- **Slack**: Empty channel shows history of what teammates did + how to contribute

**Psychology mechanism:**
- Endowment Effect: Give users something to protect (even an empty space "theirs")
- Behavioral Prompt (Fogg): Clear trigger for what to do next
- Reduce anxiety: Blank = overwhelming; guided empty = comfortable

**Implementation checklist:**
- [ ] NEVER show just a blank screen or generic "No items found"
- [ ] Include: icon/illustration + explanation headline + primary action CTA
- [ ] Match empty state to the specific context (empty search ≠ empty new user)
- [ ] For success-case empty states (inbox zero), celebrate it
- [ ] Include sample/demo content option for complex tools

**Failure modes:**
- Using same empty state for "no results" vs "nothing created yet" — different contexts
- Empty state illustration without a clear CTA — decorative but not helpful
- Not differentiating between "user has never done X" and "X was deleted"

**Success metrics:**
- Conversion rate from empty state to first action
- Time spent on empty state before action (lower is better)

---

## Pattern 1.4 — The Minimum Viable Onboarding

**What it is:**
Get users to their first value moment in the fewest steps possible. Every step is a drop-off risk.

**When to use:**
- Mobile apps where session length is short
- Consumer apps with low patience users
- Products competing against free/easy alternatives

**Real-world examples:**
- **Uber**: Sign up → payment → first ride in under 3 minutes
- **Spotify**: Listen immediately, create account later (reverse flow)
- **Pinterest**: Browse without account; account creation triggered by desire to save
- **TikTok**: Content before signup — you're hooked before they ask who you are

**Psychology mechanism:**
- Sunk Cost / Foot-in-door: Once using the product, more motivated to complete signup
- Effort Justification: Less effort = lower barrier = higher completion
- Instant Gratification: Immediate value before asking for effort

**Implementation checklist:**
- [ ] Map every step in signup flow — remove anything not strictly necessary
- [ ] Consider "sign up later" or "try first" flows
- [ ] Email/phone number should be last, not first
- [ ] Never require credit card before delivering value
- [ ] Save progress if user leaves mid-onboarding

**Failure modes:**
- Optimizing for signup completions but getting low-quality users
- "Skip" options that skip value-delivering steps
- Account required for features that don't need accounts

**Success metrics:**
- Signup funnel completion rate per step
- Time from landing to first value moment
- D7 retention of users who completed fast vs slow onboarding

---

# SECTION 2: NAVIGATION PATTERNS

---

## Pattern 2.1 — Hub & Spoke Navigation

**What it is:**
A central home screen (hub) connects to feature screens (spokes). Users always return to hub to navigate.

**When to use:**
- Mobile apps with 4-6 distinct feature areas
- Apps where content is primary (not utility)
- When users don't need cross-feature navigation

**Real-world examples:**
- **Airbnb**: Home (search) hub → listing detail spokes
- **Spotify**: Home hub → artist/album/playlist spokes; back returns to home
- **Instagram**: Feed hub → post/profile/stories spokes

**Psychology mechanism:**
- Spatial memory: Users build mental map of "center → out → back"
- Cognitive simplicity: One decision point instead of many
- Depth allows richness: Content-rich but not complex navigation

**Implementation checklist:**
- [ ] Home/hub should be the most reachable screen (tab bar position matters)
- [ ] Back button always returns to hub, not previous spoke
- [ ] Hub should provide enough value alone (not just a menu)
- [ ] Limit spoke depth to 2-3 levels maximum

**Failure modes:**
- Spokes that link to other spokes (breaks the mental model)
- Hub that's empty or purely navigational (wastes the most valuable screen)
- No clear visual signal that you're in a spoke vs hub

---

## Pattern 2.2 — Progressive Navigation Disclosure

**What it is:**
Show only top-level navigation first. Reveal sub-navigation only when user commits to a section.

**When to use:**
- Products with complex multi-level information architecture
- B2B SaaS with many feature modules
- Any app where navigation clutter is a risk

**Real-world examples:**
- **Linear**: Sidebar shows top categories; expanding reveals sub-items
- **Notion**: Left sidebar collapses pages; expanding shows hierarchy
- **Stripe Dashboard**: Top-level products; clicking reveals sub-features
- **Figma**: Left panel collapses layers; expanding reveals structure

**Psychology mechanism:**
- Hick's Law: Fewer choices = faster decisions
- Progressive Disclosure: Reveal complexity as user advances = less overwhelm

**Implementation checklist:**
- [ ] Identify the 4-6 core navigation categories maximum at top level
- [ ] Sub-navigation only appears after user selects parent category
- [ ] Breadcrumbs show current location after 2+ levels
- [ ] Collapsed state should indicate "more here" (count badge, arrow indicator)

---

## Pattern 2.3 — Contextual Navigation (Bottom Sheet)

**What it is:**
Navigation options appear from bottom based on what user is looking at, replacing a fixed navigation bar.

**When to use:**
- Content-heavy mobile apps
- When primary action changes based on current screen
- When bottom tab bar takes too much vertical space

**Real-world examples:**
- **Google Maps**: Bottom sheet expands with location details, collapses to show map
- **Apple Maps**: Floating card reveals actions relevant to selected location
- **Airbnb**: Filter sheet appears from bottom; actions change based on search vs listing view

**Psychology mechanism:**
- Context-first: Actions are relevant to what user is doing, not global
- Thumb zone optimization: Bottom position = easy reach
- Reduced cognitive load: Only relevant options shown

**Implementation checklist:**
- [ ] Default state: partially visible preview (peek) inviting expansion
- [ ] Full expand: full action set revealed
- [ ] Dismiss gesture: swipe down or tap outside
- [ ] Never remove primary navigation entirely — some global nav must persist
- [ ] Maintain state when sheet dismisses (don't reset scroll position)

---

# SECTION 3: ENGAGEMENT & RETENTION PATTERNS

---

## Pattern 3.1 — Streak Mechanics

**What it is:**
Track consecutive days/actions and display progress. Losing a streak creates motivation to maintain it.

**When to use:**
- Apps requiring daily habit formation
- EdTech, fitness, productivity tools
- Any app where regular engagement has compound value

**Real-world examples:**
- **Duolingo**: Flame streak for consecutive days of learning
- **Snapchat**: Streak count between two users creates daily check-in obligation
- **GitHub**: Green contribution graph — public social streak
- **Wordle (NYT)**: Streak count shown in stats panel

**Psychology mechanism:**
- Loss Aversion: Losing a 30-day streak feels 2x worse than the gain of maintaining it
- Variable Reward: Will I maintain my streak today? (uncertainty → engagement)
- Identity reinforcement: "I'm a person who does this every day"
- Sunk cost: 47 days invested → strong motivation not to lose

**Implementation checklist:**
- [ ] Make streak prominently visible on home screen
- [ ] Notify users before streak breaks (not after)
- [ ] Provide "streak freeze" or recovery mechanism (reduces anxiety, increases trust)
- [ ] Celebrate streak milestones (7 days, 30 days, 100 days)
- [ ] Show streak to others when social context applies

**Failure modes:**
- Streak breaks with no recovery option → user churns out of shame
- Streak that resets for wrong reasons (timezone bug, technical error) → destroys trust
- Streak mechanics without underlying value → feels manipulative

**Success metrics:**
- D30 and D90 retention (streak users vs non-streak users)
- DAU/MAU ratio
- Notification open rate for streak reminders

---

## Pattern 3.2 — Variable Reward Schedule

**What it is:**
Rewards are delivered at unpredictable intervals, creating stronger engagement than fixed reward schedules.

**When to use:**
- Gamified products
- Content discovery features
- Social feeds and notifications

**Real-world examples:**
- **TikTok**: "Pull to refresh" may show incredible or boring content → slot machine effect
- **Instagram**: Scroll may surface a viral post or nothing special → keep scrolling
- **Spotify's Discover Weekly**: New playlist every Monday — will it be great this week?
- **Duolingo**: Random bonus XP on completing exercises

**Psychology mechanism:**
- Skinner's Variable Ratio Reinforcement: Most powerful reinforcement schedule
- Dopamine release: Anticipation is as rewarding as the reward itself
- Optimism bias: "Next one might be the great one"

**Implementation checklist:**
- [ ] Identify reward opportunities (content discovery, bonuses, achievements)
- [ ] Randomize reward size and timing within acceptable ranges
- [ ] Make the anticipation visible (loading animation, reveal animation)
- [ ] Ensure rewards are genuinely variable — predictable patterns reduce effect
- [ ] Cap randomness: some sessions must feel rewarding or users churn

**Failure modes:**
- Pure randomness with no guarantee of value → users stop expecting anything
- Over-use: entire product feels like a slot machine → manipulative perception
- Variable rewards without real value → dark pattern

---

## Pattern 3.3 — Progress Visibility

**What it is:**
Show users how far they've come and how close they are to the next milestone.

**When to use:**
- Multi-step processes
- Skill/level progression
- Profile completion flows
- Long-form content consumption

**Real-world examples:**
- **LinkedIn**: Profile completion meter (40% → 70% → "All Star")
- **Duolingo**: XP bar filling toward daily goal
- **GitHub**: Contribution graph shows historical progress
- **Linear**: Issue progress bars on projects
- **Airbnb**: Progress bar during multi-step listing creation

**Psychology mechanism:**
- Goal Gradient Effect: Effort increases as users approach goal (faster completion near end)
- Endowment Effect: Partial progress feels like possession worth protecting
- Completion drive: Incompleteness creates psychological tension (Zeigarnik Effect)

**Implementation checklist:**
- [ ] Show progress relative to goal, not just absolute numbers
- [ ] Display progress on the path to a meaningful reward/milestone
- [ ] Give "boosted" start — show 10-15% completion before user does anything
- [ ] Celebrate completion moments (animation, badge, message)
- [ ] Make progress persistent across sessions

**Failure modes:**
- Progress that resets → destroys motivation and trust
- Progress bars for tasks with no clear endpoint → feels endless, demotivating
- Showing progress without revealing what the reward for completion is

---

## Pattern 3.4 — Social Proof Feed

**What it is:**
Show what other users are doing in real-time or recently to drive active engagement.

**When to use:**
- Marketplaces (show recent purchases)
- Creator platforms (show what's trending)
- Learning platforms (show peer progress)
- E-commerce (show who else is viewing)

**Real-world examples:**
- **Airbnb**: "12 people are looking at this listing right now"
- **Booking.com**: "Only 2 rooms left at this price!" + "Booked 3 times in last 24 hours"
- **ProductHunt**: Upvote counts show community validation in real-time
- **GitHub**: Star counts signal product quality

**Psychology mechanism:**
- Social Proof (Cialdini): Others' behavior reduces uncertainty about quality
- Scarcity + Social Proof combined: High demand = good → act before it's gone
- Safety in numbers: "If many did this, it must be safe/good"

**Implementation checklist:**
- [ ] Show social proof at decision points, not everywhere
- [ ] Localize proof when possible ("in your city", "by people like you")
- [ ] Use specific numbers, not vague claims ("2,847 people" not "thousands")
- [ ] Real-time proof requires accuracy — fake urgency destroys trust permanently
- [ ] Allow users to hide social proof (privacy consideration)

**Failure modes:**
- Manufactured scarcity ("Only 3 left!" when there are 300) → massive trust destruction
- Social proof that doesn't match user context (enterprise reviews for consumer product)
- Over-use → users become desensitized ("everyone says this")

---

# SECTION 4: FEEDBACK & NOTIFICATION PATTERNS

---

## Pattern 4.1 — Inline Feedback

**What it is:**
Immediate, contextual feedback appears next to the element being interacted with, not in a separate toast or modal.

**When to use:**
- Form validation
- Real-time input processing
- Password strength indicators
- Search with live results

**Real-world examples:**
- **Stripe**: Credit card number field validates format as you type, shows card type icon
- **Linear**: Inline character count on issue titles
- **Notion**: Real-time word count in documents
- **Figma**: Live coordinate/dimension display while dragging

**Psychology mechanism:**
- Immediate feedback (Fogg Behavior Model): Shortest possible time between action and confirmation
- Error prevention vs error recovery: Catch mistakes before they happen, not after
- Reduced anxiety: Constant confirmation that system understood input

**Implementation checklist:**
- [ ] Validate on blur (field loses focus), not just on submit
- [ ] For password fields: show requirements, check them off in real-time
- [ ] Inline errors appear below the field, never in a modal
- [ ] Success state should also show (green checkmark after valid email)
- [ ] Never clear user's input when showing an error

**Failure modes:**
- Validating on every keystroke → too aggressive, breaks flow
- Inline errors that disappear before user reads them
- Error messages that say "invalid input" without explaining why

---

## Pattern 4.2 — Toast Notifications

**What it is:**
Temporary, non-blocking notifications that confirm actions or deliver low-priority information.

**When to use:**
- Confirming an action completed ("Saved", "Copied link", "Sent")
- Delivering non-critical system information
- Never for: errors requiring action, important information user must see

**Real-world examples:**
- **Linear**: "Issue created" toast with undo action after creating
- **Notion**: "Link copied" after sharing
- **Vercel**: "Deployment started" confirmation
- **Stripe**: "Webhook created" after API configuration

**Psychology mechanism:**
- Closure: Confirmation closes the loop of uncertainty after an action
- Non-interruption: Toast doesn't block work, respects user flow
- Undo opportunity: Reduces fear of irreversible actions

**Implementation checklist:**
- [ ] Duration: 3-5 seconds for simple confirmation, 5-7 for with action
- [ ] Position: Bottom of screen (mobile), bottom-right or top-right (desktop)
- [ ] Include undo/action when relevant ("Issue created — View / Undo")
- [ ] Maximum 1 toast visible at a time
- [ ] Different types: success (green), error (red), info (neutral), warning (orange)

**Failure modes:**
- Using toast for critical errors user must read → may be missed
- Toast without enough time to read the full message
- Multiple simultaneous toasts (stacked) → confusing, missed
- Auto-dismiss on error that requires user action

---

## Pattern 4.3 — Smart Notification Timing

**What it is:**
Deliver notifications at the moment when they're most relevant and actionable, not just immediately when triggered.

**When to use:**
- Engagement nudges (activity reminders)
- Re-engagement campaigns
- Time-sensitive but not urgent notifications

**Real-world examples:**
- **Duolingo**: Streak reminder at the time of day when user previously studied
- **Spotify**: "Your Discover Weekly is ready" delivered Monday 8am
- **GitHub**: Digest of repository activity delivered at user's active time
- **LinkedIn**: "See who viewed your profile" at peak platform usage time

**Psychology mechanism:**
- Context matching: Notification arrives when user is in the right mindset
- Habit stacking: Trigger → existing behavior → app open
- Loss Aversion: "Your streak ends in 2 hours" creates urgency at the right time

**Implementation checklist:**
- [ ] Track user's active hours from behavioral data (not assumed)
- [ ] Segment by timezone (never notify at 3am)
- [ ] Batch non-urgent notifications into a single daily digest
- [ ] A/B test notification timing, not just copy
- [ ] Respect notification fatigue: less is more
- [ ] Provide granular notification preferences (not just on/off)

**Failure modes:**
- Notification at wrong time (activity when user is working) → annoying
- Too frequent → users disable all notifications
- Generic timing (always 9am) → predictable, ignored

---

# SECTION 5: TRUST & CREDIBILITY PATTERNS

---

## Pattern 5.1 — Progressive Trust Building

**What it is:**
Request sensitive information (financial, personal) only after delivering value that justifies the ask.

**When to use:**
- Any flow requesting payment, sensitive data, or major commitment
- Onboarding where trust is not yet established
- Marketplaces connecting strangers

**Real-world examples:**
- **Airbnb**: Show full listing details before asking guest to create account
- **Stripe**: Full documentation access before API key required
- **Revolut**: Basic features available, advanced features unlock after verification
- **Wise**: Show transfer fee transparency before requiring personal details

**Psychology mechanism:**
- Reciprocity (Cialdini): Give value first, trust is earned before ask
- Commitment-consistency: Small commitments (view listing) lead to larger ones (book)
- Transparency builds trust: No hidden requirements, no surprise asks

**Implementation checklist:**
- [ ] Map the "trust ladder" — what value must be delivered at each ask level?
- [ ] Never surprise users with requirements (no "you need to verify your identity" at checkout)
- [ ] Show what information is needed at the START of a flow, not partway through
- [ ] Explain WHY information is needed ("We need your ID to protect all users")
- [ ] Provide "save and continue later" options for high-effort processes

**Failure modes:**
- Bait-and-switch: Long flow, then requirement at the end → abandonment + anger
- No explanation for data requests → anxiety, abandonment
- KYC required before ANY value delivered → high friction for uncertain return

---

## Pattern 5.2 — Transparency in Financial Data

**What it is:**
Show the full breakdown of costs, fees, and calculations before user commits.

**When to use:**
- Any payment flow
- Subscription pricing
- Commission-based products
- Marketplace fee structures

**Real-world examples:**
- **Wise**: Shows exact amount recipient gets in their currency before transfer
- **Stripe**: Fee calculator shows exactly what you pay per transaction
- **Airbnb**: Price breakdown (room + cleaning + service fee) before booking
- **Revolut**: Real mid-market exchange rate highlighted vs competitor's hidden fees

**Psychology mechanism:**
- Anxiety Reduction: Uncertainty about costs is a major conversion blocker
- Trust through transparency: Showing fees, even if higher, builds more trust than hiding them
- WYSIWYG principle: "What I see is what I pay" → confidence to commit

**Implementation checklist:**
- [ ] Show total cost (including all fees) before final confirmation step
- [ ] Break down fee components (don't just show total)
- [ ] Compare to alternatives when favorable ("vs $12 bank fee = you save $8")
- [ ] Confirm exchange rates with timestamp ("Rate locked for 10 minutes")
- [ ] Receipt/confirmation email must match what was shown

**Failure modes:**
- Hidden fees revealed at last step → "gotcha" moment → abandonment + resentment
- Ambiguous language ("government taxes may apply") → anxiety, not trust
- Post-transaction fee surprises → chargeback, support escalation, bad reviews

---

## Pattern 5.3 — Social Validation Signals

**What it is:**
Display third-party validation (ratings, reviews, certifications, logos) at decision-critical moments.

**When to use:**
- Any conversion-critical page
- New user landing (particularly for unfamiliar products)
- High-stakes decisions (large purchase, personal data sharing)

**Real-world examples:**
- **Stripe**: Displays logos of Shopify, Lyft, Amazon as customers
- **Superhuman**: Testimonials from recognizable people at point of waitlist signup
- **Linear**: "Used by teams at [recognizable companies]"
- **Wise**: "4.6 stars, 240,000+ Trustpilot reviews" next to signup CTA

**Psychology mechanism:**
- Social Proof: Others have done this safely → it's safe for me
- Authority Bias: Recognizable logos transfer trust to unknown brand
- Risk reduction: "If OpenAI uses it, it can't be a scam"

**Implementation checklist:**
- [ ] Place logos and reviews NEAR the conversion action, not only on "About" page
- [ ] Use logos of companies users recognize and respect (not just biggest clients)
- [ ] Show review count AND rating (specificity = credibility)
- [ ] Source reviews from verified third-party platforms (Trustpilot, G2, App Store)
- [ ] Keep testimonials updated (old dates reduce credibility)

**Failure modes:**
- Testimonials that are obviously written by the company ("Amazing product! — John D.")
- Logos of clients who never actually consented → legal + reputational risk
- Review count not updated → "127 reviews from 2019" feels abandoned

---

# SECTION 6: ERROR & RECOVERY PATTERNS

---

## Pattern 6.1 — Graceful Error Recovery

**What it is:**
When errors occur, maintain user progress and provide a clear path to resolution — never send users backward.

**When to use:**
- Form submission errors
- Failed transactions
- Network failures
- Permission errors

**Real-world examples:**
- **Stripe**: If payment fails, shows exactly which field needs correction (not "error occurred")
- **Linear**: If action fails, shows inline error with specific cause + retry button
- **Airbnb**: If booking fails, shows alternative dates from the same host
- **Wise**: If transfer blocked for compliance reason, explains exactly what's needed

**Psychology mechanism:**
- Control restoration: Error is scary, but path forward restores sense of control
- Effort preservation: "Your data was saved" prevents effort loss
- Trust repair: Clear error = competent company; vague error = untrustworthy

**Implementation checklist:**
- [ ] NEVER show "Something went wrong" without specific guidance
- [ ] Format: What happened + Why + What to do next
- [ ] Preserve all user input after error — never clear a filled form
- [ ] Offer alternative action when primary fails
- [ ] Log errors with context to fix the cause, not just the message

**Error message formula:**
> ❌ Bad: "Error. Please try again."
> ✅ Good: "We couldn't process your card. The card number you entered doesn't match your billing zip code. Please check and try again — your other details are saved."

**Failure modes:**
- Generic error messages → user doesn't know what to do → abandons
- Error clears the form → user has to start over → rage quit
- Error with no recovery action → dead end

---

## Pattern 6.2 — The Undo Pattern

**What it is:**
Instead of confirmation dialogs, allow actions to be undone for a limited time after execution.

**When to use:**
- Deletions (soft-delete)
- Archive/hide actions
- Send actions (email, messages)
- Any irreversible-seeming action that can technically be reversed

**Real-world examples:**
- **Gmail**: "Undo Send" — 5-30 second window before message actually sends
- **Linear**: "Issue deleted — Undo" toast appears for 5 seconds
- **Notion**: Pages go to Trash for 30 days before permanent deletion
- **Slack**: Message edit/delete with activity log retained for admins

**Psychology mechanism:**
- Anxiety Reduction: "I can undo this if I made a mistake" → lower hesitation before action
- Action Confidence: Undo allows bolder actions → more engagement
- Reduces confirmation fatigue: No "Are you sure?" dialogs

**Implementation checklist:**
- [ ] Show undo option immediately after action (toast with "Undo" button)
- [ ] Window: 5-30 seconds for messages; 7-30 days for deletions
- [ ] Clearly communicate when the window expires ("Undo (12s remaining)")
- [ ] Soft-delete: items are hidden, not actually deleted until window expires
- [ ] Send audit trail / activity log for team products

**Failure modes:**
- Undo window too short (< 3 seconds) — missed before user reads toast
- Permanent deletion without undo for irreplaceable content — catastrophic UX
- Undo works but user doesn't know it exists

---

# SECTION 7: SEARCH & DISCOVERY PATTERNS

---

## Pattern 7.1 — Search-First Navigation

**What it is:**
Search is the primary navigation mechanism, replacing or supplementing traditional menu navigation.

**When to use:**
- Products with 50+ items or dynamic content
- Power users who know what they want
- B2B tools with complex, deep feature sets

**Real-world examples:**
- **Linear**: Cmd+K command palette is primary navigation
- **Notion**: Cmd+P search opens everything: pages, commands, people
- **Figma**: Search box finds any frame, component, or feature
- **Raycast**: Entirely search-driven Mac productivity tool

**Psychology mechanism:**
- Recognition over Recall: But with enough use, recall becomes faster than menu navigation
- Expert user optimization: Power users find search faster than 5-level menus
- Flow state preservation: Keyboard-first = no context switching to mouse

**Implementation checklist:**
- [ ] Global keyboard shortcut for search (Cmd+K is ubiquitous convention)
- [ ] Search indexes: content, commands, settings, people, recent items
- [ ] Show recent searches as default state
- [ ] Include fuzzy matching (typos, partial words)
- [ ] Show keyboard shortcuts in results (reinforces power-user behavior)

---

## Pattern 7.2 — Faceted Search & Filtering

**What it is:**
Allow users to narrow search results using multiple simultaneous filters across different dimensions.

**When to use:**
- Catalog with 100+ items
- Marketplace search (Airbnb, e-commerce)
- Any product where users have specific multi-dimensional criteria

**Real-world examples:**
- **Airbnb**: Price + dates + guests + amenities + property type — all live-filtering
- **Linear**: Filter by assignee + status + label + priority simultaneously
- **Airtable**: Filter by field + condition + value, add multiple conditions
- **Figma**: Search by name + type + page in layers panel

**Psychology mechanism:**
- Progressive filtering reduces overwhelm (Hick's Law: start with all, narrow down)
- Control and mastery: User defines the search, not algorithm
- Instant feedback: See results update in real-time → engagement

**Implementation checklist:**
- [ ] Live filter: Results update as filters are applied (not "apply filters" button)
- [ ] Show result count as filters are adjusted
- [ ] Make filters easy to remove (individual × buttons + "Clear all")
- [ ] Persist filters during session (user built them, don't reset)
- [ ] Prioritize top 3-5 most-used filters in visible area; collapse rest

**Failure modes:**
- Filters that produce 0 results without guidance on how to expand
- Filter combinations that are mutually exclusive with no warning
- Filters reset on page refresh (frustrating for power users)

---

# SECTION 8: CONVERSION PATTERNS

---

## Pattern 8.1 — Single Call to Action

**What it is:**
Each screen or section has exactly one primary action. Secondary actions are visually subordinate.

**When to use:**
- Any conversion-critical screen
- Landing pages
- Onboarding steps
- Checkout flows

**Real-world examples:**
- **Stripe**: "Start now for free" — one primary CTA per section
- **Linear**: "Start building" — one hero CTA above the fold
- **Superhuman**: "Get early access" — singular, prominent CTA

**Psychology mechanism:**
- Hick's Law: More choices = longer decision time = more abandonment
- Attention focus: One CTA = 100% attention; two CTAs split attention
- Decision relief: User knows exactly what the "right" next step is

**Implementation checklist:**
- [ ] One primary CTA per viewport (visual weight: large, colored, prominent)
- [ ] Secondary actions allowed but visually subordinate (smaller, less contrast)
- [ ] Primary CTA text describes the outcome, not the action ("Get your free report" not "Submit")
- [ ] CTA button size: minimum 44×44px (mobile), comfortable padding on desktop
- [ ] Test CTA copy — often the most impactful conversion variable

**Failure modes:**
- Two equally weighted buttons (parallel CTAs) → choice paralysis
- CTA that says "Learn More" → leads nowhere productive
- CTA without clarity on what happens next → anxiety

---

## Pattern 8.2 — Fear of Missing Out (FOMO) Mechanics

**What it is:**
Create legitimate time pressure or scarcity that motivates timely action.

**When to use:**
- Limited-time offers with genuine deadlines
- Flash sales and promotions
- Early-bird pricing
- Limited seat/capacity products

**Real-world examples:**
- **Airbnb**: "8 guests have shown interest in the past 7 days"
- **Booking.com**: "Only 1 room left at this price" (when accurate)
- **Spotify**: Exclusive live events with finite ticket availability
- **ProductHunt**: "Launching today only" for product hunts

**Psychology mechanism:**
- Scarcity Principle (Cialdini): Limited availability increases perceived value
- Loss Aversion: Fear of losing the deal = stronger motivator than gaining it
- Social proof + urgency combined: Others want this + I might miss out

**Implementation checklist:**
- [ ] ONLY use when scarcity/urgency is genuine — fake urgency destroys trust permanently
- [ ] Show countdown timers only for real deadlines
- [ ] Explain the scarcity reason ("Limited beta spots", "Event ends Friday")
- [ ] Don't use urgency on every item — diminishes impact
- [ ] Provide option to "save" or "watch" for users not ready to commit

**Failure modes:**
- Countdown timer that resets when user refreshes → obvious manipulation → trust destroyed
- "Only 2 left" when stock replenishes immediately → rage review territory
- Urgency without relevance → users learn to ignore it

---

# SECTION 9: MOBILE-SPECIFIC PATTERNS

---

## Pattern 9.1 — Thumb Zone Optimization

**What it is:**
Design primary actions to fall within the comfortable reach zone of a person's thumb when holding a phone.

**When to use:**
- All mobile app design
- Any mobile-first product

**The Thumb Zones (375px iPhone reference):**
- **Green (Easy reach)**: Bottom 40% of screen — primary CTAs here
- **Yellow (Stretch)**: Middle 30% — secondary actions acceptable
- **Red (Difficult)**: Top 30% — navigation, status, non-interactive content only

**Real-world examples:**
- **Spotify**: Play controls at bottom, near thumb
- **Instagram**: Tab bar and action buttons at bottom
- **Airbnb**: Primary search action centered at accessible level
- **TikTok**: Like/comment/share in right-thumb zone, fixed vertically

**Implementation checklist:**
- [ ] Primary CTA: bottom quarter of screen minimum on mobile
- [ ] Destructive actions (delete): require two-handed interaction or extra confirmation
- [ ] Navigation: bottom tab bar (iOS/Android pattern), not hamburger top-left
- [ ] Minimum touch target: 44×44px (Apple) / 48×48dp (Google)
- [ ] Critical actions never require left-hand-only reach on a right-handed phone

---

## Pattern 9.2 — Gesture-First Interaction

**What it is:**
Replace visible buttons with gestures for power users, but always maintain a visible alternative.

**When to use:**
- Productivity apps used repeatedly
- After users have been using the app for 7+ days
- When screen space is at premium

**Real-world examples:**
- **Email apps**: Swipe left to archive, swipe right to delete (vs buttons)
- **TikTok**: Swipe up for next, swipe right to go back (vs arrow buttons)
- **Airbnb**: Swipe through listing photos (vs arrow tap buttons)
- **Notion**: Long press to drag-reorder blocks

**Psychology mechanism:**
- Efficiency for experts: Gestures are faster than locating and tapping a button
- QWERTY effect: Unintuitiveness becomes invisible through repetition
- Flow state: Gesture-first removes friction for habitual actions

**Implementation checklist:**
- [ ] Always provide a visible alternative (button) for any gesture
- [ ] Visual affordance: show what gestures are available (peek, arrow, hint)
- [ ] Onboarding: introduce gestures with one-time coach marks
- [ ] Don't use the same gesture for different actions in different contexts
- [ ] Confirm destructive gesture-triggered actions (swipe-to-delete → undo toast)

---

# SECTION 10: AI FEATURE INTRODUCTION PATTERNS

---

## Pattern 10.1 — AI as Assistant, Not Replacement

**What it is:**
Position AI features as augmenting user control, not replacing user decision-making.

**When to use:**
- Any AI feature launch
- Products where user expertise and control are valued
- B2B tools where users need to explain AI outputs to others

**Real-world examples:**
- **Notion AI**: "Help me write" places AI as collaborator; user remains author
- **Figma AI**: "Generate" suggestions that user then edits — never auto-applies
- **Linear**: AI-suggested issue titles — user always confirms before saving
- **GitHub Copilot**: Suggestions shown as ghost text; Tab to accept, keep typing to ignore

**Psychology mechanism:**
- Autonomy (Self-Determination Theory): Control over outcome = satisfaction
- Trust calibration: Users distrust AI that acts without permission
- Perceived competence: User feels smart for directing AI, not replaced by it

**Implementation checklist:**
- [ ] AI output always requires user confirmation before final action
- [ ] Show "AI generated" label — never pass AI content as user's own without consent
- [ ] Provide easy "regenerate" and "edit" options post-generation
- [ ] Allow users to adjust AI intensity (off/suggestions only/full generation)
- [ ] Explain why AI made a specific recommendation ("Based on your last 3 campaigns...")

**Failure modes:**
- AI that auto-saves or auto-posts without confirmation → loss of trust
- AI output with no editing capability → user feels imprisoned
- No way to turn AI off → alienates users who don't want it

---

## Pattern 10.2 — Transparent AI Confidence

**What it is:**
Communicate when AI is confident vs uncertain, and allow users to verify important AI decisions.

**When to use:**
- AI-generated recommendations for consequential decisions
- Financial, medical, or legal AI suggestions
- Any AI decision where being wrong has significant user impact

**Real-world examples:**
- **Stripe Radar**: Shows fraud risk score with reasoning ("This card was used in 3 countries in 24 hours")
- **Linear**: AI priority suggestions include reasoning visible on hover
- **Notion AI**: "I'm not sure about this — please verify" for factual claims
- **Figma**: AI suggestions show similarity score to existing design system components

**Psychology mechanism:**
- Epistemic transparency: Knowing AI uncertainty = calibrated trust (more healthy than blind trust)
- Control restoration: "I can check this" = confidence to use AI recommendations
- Error expectation setting: Users accept AI errors when inherent uncertainty is communicated

**Implementation checklist:**
- [ ] Show confidence indicators on AI outputs when stakes are high
- [ ] Provide reasoning/explanation for AI decisions (not just the decision)
- [ ] Link to source data when AI makes factual claims
- [ ] Allow users to flag incorrect AI outputs for improvement
- [ ] Never overstate AI accuracy in product copy or UI

---

# APPENDIX: BEHAVIORAL SCIENCE QUICK REFERENCE

| Principle | Definition | UX Application |
|-----------|-----------|----------------|
| **Loss Aversion** | Losses feel 2× more painful than equivalent gains feel good | Streak breaks, expiring discounts, "don't lose your progress" |
| **Fogg Behavior Model** | Behavior = Motivation × Ability × Prompt | Remove friction (ability), add triggers (prompt) at high motivation moments |
| **Cognitive Load** | Working memory can hold 7±2 chunks of information | Progressive disclosure, simple navigation, inline help |
| **Goal Gradient Effect** | Effort increases as goal approaches | Show progress bars, especially when near completion |
| **Zeigarnik Effect** | Incomplete tasks stay more active in memory than complete ones | Profile completion nudges, progress saves, "resume where you left off" |
| **Social Proof** | Uncertainty → look to others' behavior | Review counts, user counts, activity feeds, "X people viewing" |
| **Scarcity** | Limited availability increases perceived value | Genuine limited offers, capacity-based urgency |
| **Reciprocity** | Giving first creates obligation to give back | Free value before asking for account/payment |
| **Fitts's Law** | Time to acquire target ∝ distance/size | Large touch targets, bottom-of-screen primary CTAs |
| **Hick's Law** | Decision time ∝ log of number of choices | Single CTAs, progressive disclosure, filtered search |
| **Jakob's Law** | Users expect your app to work like apps they know | Follow platform conventions (iOS/Android/Web standards) |
| **Peak-End Rule** | Experience judged by peak moment + final moment | Design wow moments + strong success/completion states |
| **Variable Reward** | Unpredictable rewards drive stronger engagement than fixed ones | Content feeds, achievement systems, discovery features |

---

*This document covers UX patterns (behavior, psychology, flows, strategy).*
*For UI patterns (colors, typography, components, visual design) see: UIUX_Combined_for_Gem.md*
