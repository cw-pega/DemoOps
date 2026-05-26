# All In Logistics — hazard recall demo

## What this demo is for
A live event demo built for Pega World 2025 (Las Vegas). It runs on a kiosk-style screen
and is presented by a DemoX team member to a business stakeholder audience — typically
CPG or logistics decision-makers at a trade show floor setting.

The demo closes the Pega World "All In" theme with a concrete enterprise scenario,
then lands on Blueprint's value proposition as the final beat.

## The scenario
**Company:** All In Logistics — a fictional enterprise logistics operator.
The name was chosen deliberately for the Las Vegas double meaning ("all in" = poker)
while still reading as a credible B2B brand. Do not change the company name.

**Trigger event:** A hazardous materials mislabelling incident has been detected across
a batch of shipments. A recall needs to be initiated, tracked, and resolved across
multiple carriers and depots.

**What the demo shows:**
1. An alert surfaces in the Pega case management UI — mislabelled hazmat batch detected
2. A case is automatically created and routed to the logistics ops team
3. Affected shipments are identified and flagged across the network
4. Resolution steps are assigned and tracked through to closure
5. Final screen pivots to Blueprint: "This entire workflow was designed in Blueprint
   in under a day — not months of configuration."

## Narrative and tone
- **Enterprise, not sci-fi.** An earlier version of this demo used a "Galactic Shipping"
  space-themed scenario. That was deliberately replaced. Keep all framing grounded in
  real-world CPG/FMCG logistics. No space references, no fictional future settings.
- The audience is a business stakeholder, not a developer. Avoid showing raw config,
  rules, or code. Show outcomes, not mechanics.
- Confident and calm. This is a well-run operation catching a problem early — not a crisis.

## Design decisions
- Colour palette: deep navy and signal amber. Conveys industrial reliability with urgency
  accents on the alert states.
- The final Blueprint slide should feel like a natural reveal, not a hard sell.
  Tone: "this is what modern process design looks like."
- Duration target: 8 minutes guided. Keep individual screens uncluttered — the presenter
  carries the narrative, the screen supports it.

## Known constraints
- **Not iframe-safe.** The demo cannot be embedded in an iframe due to CSP headers on
  the hosting environment. It must be opened as a standalone URL.
- Built for a 1920x1080 kiosk screen. Do not optimise for mobile.
- No live Pega connection — this is a fully self-contained HTML demo with no backend calls.

## How to regenerate or extend
Open this file alongside the demo's `index.html` in Claude Code and say:
"Using the context in claude.md, [describe your change]."

For example:
- "Add a fourth screen showing the carrier notification step"
- "Update the company name references throughout"
- "Adapt this for a healthcare vertical with a medication recall scenario"

## Last updated
2025-05-26 — Clare, DemoX AMS
