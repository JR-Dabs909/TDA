# Haven & Hound — Status Snapshot

_Last updated: 2026-10-14, after a full 7-agent store audit (catalog, operations,
finance, marketing, growth, customer-service, media QC) plus same-day fixes.
Update this file as state changes instead of letting it live only in chat._

## 2026-10-14 full audit — headline findings and fixes applied

**Fixed today (cloud session, confirmed live):**
- ShellNest, TagTrail, PawTrim handles rewritten to remove cat/kitten references
  (text-level dogs-only fix; photos still unverified — see media QC below).
- FAQ page and Contact page corrected: free-shipping threshold was wrongly
  listed as $50 (real rule is $35); Contact page was missing the phone number.
- "Collars, Tags & Leashes" smart-collection rule fixed (was matching "Lead" only,
  missed "Leash" — added, so DualGrip and PlumLoop leashes are now included).
- TrailVest and Trailside Poop Bag Dispenser removed from the "Ships Fast from
  the US" collection — both honestly disclose 7-14 day international shipping
  in their own copy, directly contradicting that collection's promise.
- 4 unverified health/behavioral-claim rewrites applied: SmartSight Timed Pet
  Feeder, QuietPaws Nail Grinder, Calming Cuddler Cozy Donut Bed (copy only,
  product names unchanged), and PawPace (renamed from "...Anti-Choking..." to
  "PawPace Slow Feeder Dog Bowl" — body copy was already clean, only the title
  carried the claim).
- 1 of 3 active, undisclosed Meta ad campaigns paused ("Haven & Hound," $20/day).
  **"First Contact" ($10/day) and the campaign carrying the false 20-25%
  discount-claim ads ($5/day) are STILL ACTIVE** — Adspirer's tool quota ran out
  mid-fix (resets Nov 3). Needs an alternate pause path (Meta Business Suite
  directly, or retry once quota resets) — this is not resolved, flag every
  session until it is.

**Confirmed NOT fixable from a cloud session (needs the browser-control
session or the owner directly) — see the 2026-10-14 browser handoff:**
- Shipping/Refund/Terms/Privacy policy page text (wrong $50 threshold on
  Shipping Policy, broken misspelled mailto links on Refund Policy, unfilled
  "[LINK]"/"[NOTE TO MERCHANT]" template placeholders on Terms of Service, a
  dead opt-out link on Privacy Policy) — blocked by a missing
  `write_legal_policies` API scope on this session's token, confirmed via a
  direct mutation attempt, not assumed.
- All visual/photo QC (RollQuest's baked-in "PROMOTE DOG'S HEALTH" image claim,
  re-verifying ShellNest/TagTrail/PawTrim's actual photos, a broader pass) —
  cdn.shopify.com is network-blocked from this cloud environment, confirmed 4
  independent ways across two separate audit passes.
- Zendrop billing status, AppLovin spend, Pinterest ad verification, Google
  Merchant Center domain-verification status, Zeely credit balance — none
  reachable via any tool/connector in this session.

**New findings, not yet actioned (need an owner decision):**
- **Printify confirmed as a live, actively-used second fulfillment supplier**
  for the apparel/merch line (5 of 7 Shopify delivery profiles are
  Printify-specific, real products route through it) — never disclosed before
  this audit, hits the CJ-only standing rule directly. Needs a decision: known
  exception, or needs winding down.
- **Collective** (Shopify's own merchant-to-merchant network) and **Avada
  Product Feed** also found installed with broad write scopes, previously
  undocumented, not wired to any channel yet — same category of risk as
  Printify, lower urgency.
- **Microsoft Copilot and Meta AI and Muse are live, auto-publishing sales
  channels** with the entire catalog (103/103) on each, zero review gate —
  unlike Amazon-CED (dormant), these are actively firing right now. Not yet
  reviewed or pulled back.
- **Phantom inventory confirmed systemic**, not just ShellNest/CordCozy: 77-85
  of ~98 active products show implausible thousands-to-millions "available"
  quantities, because no dedicated US-warehouse location exists in Shopify to
  cap it against real CJ stock. Needs a structural fix (new location + real
  per-SKU caps) — sign-off needed before touching it, given the scope.
- **5 of the 6 products previously logged below as "blocked, owner decision
  pending" are actually ACTIVE** (Summit, Night-Trail, PureFlow, Orthopedic,
  and "LED Luminous" which is now live as NightGlow Rechargeable LED Dog
  Collar) — all with honest (not false) slow-shipping disclosure, but this
  means either the decision happened off-record or they went live without the
  review this file says is still pending. Only CalmLick remains in draft.
  34 total active products (not 6) carry this same honest
  international/slow-shipping copy — see the full audit file for the list.
- **Zendrop no longer appears in the installed-apps list at all** (18 apps,
  confirmed complete) — may have been uninstalled, but the "usage charges"
  claim below is unverified either way; Shopify's Billing page isn't reachable
  by any tool here.

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
  **2026-10-13 full setup audit found 8 stacked items blocking a real sale.
  2026-10-14: owner reports all 8 resolved** (proof of address, W9, category
  qualification, payments account linked, shoppable-video product tagging,
  carrier mapping, shipping handling-time/policy pages, duplicate pixel/
  catalog cleanup). This is owner-reported, not independently re-verified by
  Claude — these items live behind TikTok's Seller Center login, which no
  tool in the cloud session can reach; a browser-control session handled the
  checks. **Caveat:** a live Shopify query on 2026-10-14 did not show TikTok
  in the store's installed-app list, which doesn't match "connected" — this
  may just be the wrong API (sales channels can live outside
  `appInstallations`), but it's unconfirmed and worth a real check next time
  anyone has TikTok Shop live in front of them.
  Original list, for reference: proof of address, W9, a possible Pet
  Supplies category gate, payout account linkage, TikTok Shop product
  tagging not carrying over from Metricool's posting API, carrier mapping,
  handling-time/policy pages, and duplicate pixel/catalog (`shopify1` 429
  items / `shopify2` 1,042 items, cleanup only, never a blocker).
- **Amazon:** see Open Issues above (dormant channel, not connected).
- **New-channel plan (growth research, nothing purchased/applied for):** eBay
  first (net $4.29/unit on the $19.99 example, $0 fee, policy explicitly
  allows wholesale dropshipping) → Walmart Marketplace in parallel ($4.31/
  unit, $0 fee, 1-4wk verification, unconfirmed if CJ is a listed Walmart
  Solution Provider — check with CJ support before applying) → Amazon skipped
  (seller-of-record requirement is structurally hard to satisfy with CJ
  fulfillment; suspension risk). All route through Shopify Marketplace Connect,
  Shopify stays the single order source.
- **Domain: purchased 2026-10-14 — havenandhound.store ($9/yr, cheaper and a
  better brand match than the originally recommended gethavenandhound.com).**
  Needed for Google Merchant Center domain verification (see Google &
  YouTube channel below). **Not yet confirmed set as primary domain** —
  Shopify's `shop.primaryDomain` still showed `havenandhounds.myshopify.com`
  as of 2026-10-14; no API exists to list all connected domains to check this
  further from a cloud session. Owner should confirm in Shopify Admin →
  Settings → Domains.
- **Google & YouTube channel: now installed and connected** (102/103 products
  staged) — this was "pending" in an earlier version of this file. Whether
  Merchant Center's domain verification is actually complete is unconfirmed
  (no tool/API can check it) — needs a direct check on that screen.
- **eBay: Marketplace Connect installed, eBay seller account connected**
  (`havenandhound`), listing sync in progress as of 2026-10-14. 0/98 active
  products have a UPC/GTIN/barcode populated — plan is to request a GTIN
  exemption during eBay listing setup rather than fabricate barcodes.
- **Walmart: on hold** — Walmart requires 2-day shipping with no lag-time
  exemption for third-party-dropship sellers like CJ; CJ's own processing
  time (1-6 days before even shipping) will likely miss that window
  regularly. Same risk shape as the Amazon seller-of-record problem. Revisit
  once eBay has an order/fulfillment track record.
- **AppLovin:** already installed as a Shopify app (discovered, not previously
  tracked). Research into cost/fit/comparison to Meta/TikTok/Google was
  in progress when the bridge session ran out of usage credits — not
  completed.

## Marketing
- **Organic-only, confirmed standing policy** (owner: "no paid campaigns or
  organic" → clarified "only organic"). A TikTok paid campaign ("Haven & Hound
  - Seat Belt Boost," $25 budget, $20 spent, 57 TikTok-reported "conversions"
  vs. 0 real Shopify orders — mistracked, not real sales) was found running
  against this rule and has been paused — **independently re-confirmed still
  paused on 2026-10-14.**
- **2026-10-14: a second, bigger, previously-undisclosed violation found.**
  3 Meta (Facebook/Instagram) campaigns active since mid-September, $35/day
  combined ($25+ spent, likely more — data was stale), on ad account
  `1588260336332921`. One of the three campaigns also runs 2 ads with false
  discount claims ("25% off"/"20% off" — only real codes are WELCOME10/
  HAVEN10, both 10%). **1 of 3 campaigns paused same day ("Haven & Hound,"
  $20/day); the other 2 ($10/day "First Contact" + the $5/day false-discount
  campaign) are still ACTIVE** — pause tooling hit its quota mid-fix (resets
  Nov 3). Needs completing via another path. The video creative for these ads
  was produced through Zeely — contradicting the "no further credits spent"
  line below; needs reconciling.
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
