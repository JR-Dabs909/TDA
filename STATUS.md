# Haven & Hound — Status Snapshot

_Last updated: 2026-10-13, after the TikTok Shop setup audit completed
post-reset. Update this file as state changes instead of letting it live only
in chat._

## Store
Shopify Basic plan, `havenandhounds.myshopify.com`. Support email
`HavenandHound.support@gmail.com`. Judge.me installed, 0 reviews (no sales
history yet — not broken).

## Catalog
- 45-product CJ "US local" batch imported. 26 activated and live:
  BloomKnit, BreezeFit, BreezePup, CarCozy, CleanStride, CozyCover, DaySnug,
  DryPod, DualGrip, FruitFit, GripTag, GroomLift, PackPal, PawStep, PlumLoop,
  PoopPro, ScrumPup, SeatShield, SlowBite, SnowDrift, SoftLoop, SoftSpot,
  StripeSnug, TidyPaws, TreatTower, VelvetBow.
- 13 older pilot/ad-image products already active before this batch: MightyArc,
  FurSweep, LiftEase, BrightLoop, CozyCoat, TrailPaw, BrushPen, MonsterChew,
  SpinFeast, MistBrush, GroomMate, SnugVest, SnuggleSuit. (26 + 13 = 39 active.)
- Blocked in DRAFT, new batch: PawTrim (cat in main image), RollQuest
  (unverifiable "PROMOTE DOG'S HEALTH" claim baked into image), TagTrail
  collar `15421303554291` (cat photo, needs owner go-ahead to crop + activate),
  WarmPup coat `15420324380915` (intentional owner hold), ShellNest bed
  `15421306798323` and CordCozy bed `15420326772979` (priced, but blocked on
  phantom-inventory issue — see Open Issues).
- Blocked, older separate batch (6 products, none activatable as-is): Summit
  Service Dog Vest Harness, Night-Trail LED Collar Light, PureFlow Filtered
  Water Fountain, Orthopedic Full-Surround Comfort Bed (all: slow 7-14 day
  non-US shipping copy), CalmLick Suction Lick Mat (0 inventory everywhere),
  LED Luminous Pet Dog Collar Night (never brand-ified, raw CJ listing).
  **Open decision for owner: fix all 6, or shelve permanently.**
- Trailside Poop Bag Dispenser: pulled to DRAFT — live listing falsely claimed
  US shipping; actually ships from China (7-14 days). Needs shipping-copy fix,
  then reactivate.
- Pricing-formula violations found and fixed, confirmed live: Trailside Poop
  Bag Dispenser, BouncePro Fetch Toy Ball, FurLift Pet Hair Remover Mitt
  (including the 3-Mitt variant, $16.99 → $22.99).

## Open issues
- **Phantom inventory (needs a broader audit):** ShellNest/CordCozy show
  10,000-50,000+ "available" per variant in Shopify even on variants CJ
  confirms have 0 real US stock. No separate US-warehouse location is
  configured in Shopify to prevent overselling. Finance independently flagged
  the same implausible-inventory pattern elsewhere. Treat as likely systemic
  until checked across the full catalog.
- **MistBrush low stock:** only 15 units left in the CJ US warehouse. Move to
  DRAFT if it sells out before restock.
- **CJ CAPTCHA wall:** cjdropshipping.com is behind bot/human verification.
  Operations and finance both correctly declined to bypass it. Owner needs to
  clear it manually in their own Chrome and confirm still logged in before CJ
  payment status, tracking, and support-ticket checks can finish.
- **Amazon Channel - CED:** a Shopify sales-channel app installed in June, but
  Amazon Seller Central itself was never connected (confirmed abandoned —
  3 unanswered CedCommerce nag emails). Not costing anything, not selling.
  Risk: 91 of 104 products are staged to it and would auto-publish unreviewed
  the instant a real Amazon account connects. A protective unpublish attempt
  was blocked by Shopify's own MCP safety policy (`publishableUnpublish`
  refused outright, no workaround). **Open decision for owner:** uninstall the
  app entirely (removes the risk, nothing lost since there's no live Amazon
  account), or leave it as a known landmine.
- **Zendrop app:** shows usage charges despite CJ being the only intended
  supplier (rule: CJ-only). Needs operations to confirm it isn't actually wired
  into fulfillment anywhere, and resolve the charge.

## Sales channels
- **TikTok Shop:** connected and properly Shopify-synced (not a duplicate-order
  risk) — confirmed by checking which products are actually published through
  it. 7 products passed TikTok review: Logo Tee, Crest Hoodie, Fleece Hoodie,
  Beanie, ChillPad, ShedAway, TrailVest. Shop itself is live/functional (30
  active listings at last check), under normal new-seller probation limits.
  **2026-10-13 full setup audit: three separate, stacked problems all have to
  clear before a real sale can happen — not one bug.** Prioritized order:
  1. **Proof of address** (owner-only) — rejected Sep 27, needs bank statement/
     lease/utility bill in owner's legal name+address, resubmitted via Seller
     Center → Settings → Qualification Center. No confirmation email exists
     either way — owner needs to check that page directly.
  2. **W9 tax info** (owner-only) — still outstanding (0/1) on the Seller
     Center dashboard.
  3. **NEW, unverified — possible third gate:** Pet Supplies may be one of
     TikTok's gated categories requiring separate category-level approval
     beyond the account-level documents above. Nobody has checked this
     specifically yet. Owner check: Seller Center → Account Health →
     Category Qualifications.
  4. **NEW, unverified — payout account:** whether a bank account is actually
     linked in Shop → Payments is unconfirmed. If never completed, a sale
     could go through and simply never pay out, silently. Owner check: Shop
     settings → Payments.
  5. **NEW — highest-impact finding, confirmed via TikTok's own help docs:**
     even once qualified, there is likely **no purchase path on any video
     posted so far.** Product tagging happens natively in the TikTok app at
     post time; tagged links do not carry over from organic posting tools,
     and there's no evidence Metricool can attach TikTok Shop product tags
     through its publishing API. Practical read: every video published via
     Metricool so far almost certainly has zero product link — no in-app way
     to buy regardless of content volume. Owner check: Shoppable video
     section for a retroactive "Link Products" tool (may only cover videos
     from the last 30 days) — unconfirmed, needs owner to look and report
     back.
  6. **Shipping carrier mapping — confirmed unconfigured** (seen directly in
     an owner screenshot). Breaks tracking sync to TikTok even on orders that
     do go through. Needs owner to open Fulfillment → Carrier Mapping; Claude
     drafts the exact Shopify-carrier → TikTok-carrier pairing once open.
  7. **Shipping handling-time / policy pages** — unconfirmed whether these
     were customized or left at TikTok's bare defaults. Lower priority.
  8. **Duplicate pixel + duplicate catalog** (`shopify1` 429 items /
     `shopify2` 1,042 items, both 100% TikTok-approved) — confirmed data
     hygiene only, not a sales blocker. Lowest priority.
- **Amazon:** see Open Issues above (dormant channel, not connected).
- **New-channel plan (growth research, nothing purchased/applied for):** eBay
  first (net $4.29/unit on the $19.99 example, $0 fee, policy explicitly
  allows wholesale dropshipping) → Walmart Marketplace in parallel ($4.31/
  unit, $0 fee, 1-4wk verification, unconfirmed if CJ is a listed Walmart
  Solution Provider — check with CJ support before applying) → Amazon skipped
  (seller-of-record requirement is structurally hard to satisfy with CJ
  fulfillment; suspension risk). All route through Shopify Marketplace Connect,
  Shopify stays the single order source.
- **Domain:** havenandhound.com / havenandhounds.com / shophavenandhound.com
  all confirmed taken by third parties. Recommended: buy gethavenandhound.com
  (~$16/yr via Shopify) and point it at the existing myshopify.com domain —
  no separate store is justified. Not purchased yet, awaiting owner go-ahead.
- **AppLovin:** already installed as a Shopify app (discovered, not previously
  tracked). Research into cost/fit/comparison to Meta/TikTok/Google was
  in progress when the bridge session ran out of usage credits — not
  completed.

## Marketing
- **Organic-only, confirmed standing policy** (owner: "no paid campaigns or
  organic" → clarified "only organic"). A TikTok paid campaign ("Haven & Hound
  - Seat Belt Boost," $25 budget, $20 spent, 57 TikTok-reported "conversions"
  vs. 0 real Shopify orders — mistracked, not real sales) was found running
  against this rule and has been paused.
- **Organic posting is live via Metricool** (confirmed schedule as of
  2026-10-12): founder note, LiftEase strap, this-or-that poll, StripeSnug
  sweater video, Aurora LED harness, BrightLoop reflective harness, PawStep
  ramp, RoadGuard x2 — FB/IG (+TikTok on video posts), autoPublish on. This
  supersedes an earlier plan to post manually via the Claude-in-Chrome
  extension, which hit a persistent multi-device pairing failure and was
  abandoned in favor of Metricool scheduling.
- **Zeely AI-avatar video plan: shelved entirely.** The owner wanted the
  AI-disclosure label removed from a finished avatar video under real
  financial pressure (one-person shop, 2 months with no traction); Claude held
  the line per CLAUDE.md rule 3 and offered zero-cost alternatives instead.
  All 3 avatar videos shelved, no further Zeely credits spent. Plan rebuilt
  around owner-filmed content:
  - **Next up, ready to shoot:** BrightLoop harness flashlight demo — phone +
    flashlight + harness in a dark room, ~20 sec, shot list already drafted,
    no AI label needed (genuinely owner-filmed). **Blocked on owner actually
    filming it.**
  - Backups queued: BrushPen toothbrush twist-demo, MightyArc chew-flex-and-
    rinse demo (both filmable without a dog).
  - Unaffected and ready whenever: 3 Pinterest pins (reuse existing images),
    Threads/Facebook text posts (no video needed).

## Permissions / environment notes
- Owner was setting up a `/permissions` allow-list on their own PC for Shopify
  write tools (`graphql_mutation`, `bulk-update-product-status`,
  `update-product`) to stop auto-mode-classifier blocks. Status unconfirmed —
  this has to be done from an interactive terminal on the owner's machine, not
  from a cloud session.
- The account hit its weekly Claude usage limit while mid-way through a
  "complete store audit, install whatever's needed" dispatch across all six
  agents — that dispatch was not completed. Resume it only after budget resets
  (2026-10-13 ~12:00 PM), and scope it down rather than firing all six agents
  fully in parallel again.
