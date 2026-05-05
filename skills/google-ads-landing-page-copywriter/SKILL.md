# Google Ads Landing Page Copywriter

**Create high-converting landing page copy for paid ads**

Writes landing page copy designed specifically to convert Google Ads traffic: tight CTA, minimal friction, proof-focused.

---

## What It Does

Executes Phase 3.2b of service fulfillment: Creates landing page copy optimized for conversion from paid ads traffic.

**Input**: Offer strategy + messaging angles + conversion objective

**Output**: Landing page headline, subheadline, body copy, form copy, CTA variants

---

## Execution

### Stage 1: Above-the-Fold Copy (1 day)
- **Headline**: Restate the ad promise + specificity
- **Subheadline**: Reinforce offer + key benefit
- **Hero image directive**: What visual proof should show?
- **Primary CTA**: Clear, action-oriented, stands out

### Stage 2: Body Copy (1 day)
- **Section 1: Social Proof** (testimonials, stats, social icons)
- **Section 2: Address Objections** (warranty, expert credentials, secure form)
- **Section 3: Urgency/Scarcity** (limited spots, time-sensitive, social proof)
- **Section 4: Final CTA** (reinforces main offer + urgency)

### Stage 3: Form & CTA Variants (0.5 days)
- **Form design suggestions** (how many fields? which ones?)
- **CTA button text variants** (test multiple versions)
- **Thank you page copy** (what happens after conversion?)

**Approach**: Minimal friction + maximum confidence

---

## Input Format

```json
{
  "offer_strategy": {
    "primary_offer": "...",
    "offer_usp": "...",
    "risk_reversal": "...",
    "messaging_angles": [...]
  },
  "conversion_objective": "lead_capture",
  "target_audience": {...}
}
```

---

## Output Format

```markdown
# Landing Page Copy - [Offer Name]

## Above The Fold

**Headline**: [Specific, benefit-focused, offer-related]

**Subheadline**: [Reinforces offer + key benefit + urgency]

**Primary CTA Button**: "[Action verb] [Specific outcome]"

**Hero Image**: [What should show? (before/after, process, trust signals, etc.)]

## Body Copy Section 1: Proof + Confidence

**Section Headline**: [Why should I trust you?]

[Proof elements]
- Stat or testimonial 1
- Stat or testimonial 2
- Trust signal 3 (ratings, credentials, etc.)

## Body Copy Section 2: Objection Handling

**Section Headline**: [Addressing common concerns]

**Objection 1**: [Common fear] → [Solution]
**Objection 2**: [Common doubt] → [Proof]
**Objection 3**: [Common concern] → [Guarantee]

## Body Copy Section 3: Urgency & Scarcity

**Section Headline**: [Why now?]

- Limited offer availability
- Time-sensitive element
- Social proof (how many booked?)

## Final CTA Section

**Headline**: [Final commitment phrase]

**Copy**: [One more reason to act + final reassurance]

**CTA Button**: "[Action verb] Now"

## Form Design Recommendation

**Minimum fields** (to reduce abandonment):
- [ ] Name
- [ ] Phone
- [ ] Email

**Optional fields** (if lead quality critical):
- [ ] How did you hear about us?
- [ ] Service needed

## CTA Button Variants (A/B Test)

**Variant 1**: "Book Free Inspection"
**Variant 2**: "Get Your Free Quote"
**Variant 3**: "Schedule Now"

## Thank You Page Copy

**Headline**: [Confirmation + what happens next]

**Copy**: [Next steps, timeline, reassurance]

**Follow-up CTA**: [Secondary action, e.g., "See our process"]
```

---

## Copy Principles for Paid Landing Pages

✍️ **Tight & focused**
- One primary CTA
- Minimal navigation
- Distraction-free design

✍️ **Ad promise match**
- Landing page headline mirrors ad copy
- Visitor sees exactly what was promised
- No surprise or confusion

✍️ **Friction minimization**
- Minimal form fields (name, phone, email only)
- Clear next steps
- Remove distracting links

✍️ **Proof-heavy**
- First third of page is social proof
- Testimonials with photos
- Specific stats/numbers

---

## Success Criteria

✅ **Headline matches ad copy** (visitor doesn't feel bait-and-switched)  
✅ **Primary CTA is clear** (no ambiguity about next step)  
✅ **Form is minimal** (3-5 fields max)  
✅ **Proof elements prominent** (testimonials, ratings, stats early)  
✅ **Copy is benefit-focused** (not feature-heavy)  
✅ **Urgency/scarcity present** (why act now?)  

---

## Feeds Into

- Design team (copy becomes page structure)
- Development team (copy becomes actual page)
- google-ads-campaign-prep-agent (uses final copy for QA)
