# Data Context Models

Structured data objects passed between skills throughout the fulfillment workflow.

---

## Overview

Context objects are JSON structures that encapsulate all findings from one skill so downstream skills inherit full context. This prevents information loss and ensures consistency across phases.

**Key principle**: Upstream data flows forward, never backward.

---

## 1. Positioning Context

**Source**: website-post-onboarding-agent  
**Consumers**: Every downstream skill (website, ads, SEO, reporting)  
**Mutability**: Read-only (never modified after Gate 1 approval)

```json
{
  "context_type": "positioning",
  "generated_by": "website-post-onboarding-agent",
  "client_name": "Clean Cut Gutters",
  "timestamp": "2026-05-04T10:30:00Z",
  
  "positioning_statement": "The gutter service for busy professionals who demand same-day reliability",
  
  "messaging_pillars": [
    {
      "pillar": "Speed",
      "description": "Same-day or next-day service for 95% of calls",
      "proof": "Founder manages operations personally to ensure delivery"
    },
    {
      "pillar": "Reliability", 
      "description": "Licensed, insured, and backed by lifetime guarantee",
      "proof": "20+ years industry experience + 4.8★ rating"
    },
    {
      "pillar": "Local Expertise",
      "description": "20+ years of founder experience + deep community roots",
      "proof": "Founded business, grew to 4-person team through word-of-mouth"
    }
  ],
  
  "target_audience": {
    "segment_name": "Busy Professionals",
    "demographics": {
      "age_range": "40-65",
      "income": "$75K-150K annually",
      "location": "Chicago suburbs, 30-mile radius"
    },
    "psychographics": {
      "values": ["Time", "Reliability", "Local relationships", "Quality over price"],
      "pain_points": [
        "Forget to schedule maintenance",
        "Fear of heights/ladder safety",
        "Don't know who to trust",
        "Bad experiences with unreliable contractors"
      ],
      "decision_criteria": [
        "Local presence & recommendations (80%)",
        "Reputation & reviews (75%)",
        "Speed of service availability (60%)",
        "Warranty/guarantee (55%)"
      ]
    },
    "behavior": {
      "search_patterns": ["gutter cleaning near me", "best gutter service chicago"],
      "decision_triggers": ["Water damage fear", "Seasonal (spring/fall)"],
      "research_methods": ["Google reviews", "Neighbor recommendations", "Online reputation"]
    }
  },
  
  "unique_differentiators": [
    {
      "differentiator": "Same-day service",
      "proof": "95% of calls completed within 24 hours",
      "competitive_advantage": "Pro Gutter Pros claims this; we add reliability",
      "defensibility": "Operationally proven"
    },
    {
      "differentiator": "Local expertise",
      "proof": "20+ years founder experience",
      "competitive_advantage": "Most competitors are franchises",
      "defensibility": "Founder track record"
    },
    {
      "differentiator": "Lifetime guarantee",
      "proof": "Clog-free for life of ownership",
      "competitive_advantage": "Unique claim in market",
      "defensibility": "Risk reversal + confidence in work"
    }
  ],
  
  "proof_points": [
    "20+ years in gutter systems (industry expert)",
    "Built business from side project to 4 employees through word-of-mouth",
    "4.8★ Google rating from 200+ reviews (social proof)",
    "Same-day capability (proven operational strength)"
  ],
  
  "competitive_landscape": {
    "competitors_analyzed": 6,
    "positioning_gap": "No competitor combines speed AND local expertise",
    "strategic_advantage": "Fills unique market gap"
  }
}
```

---

## 2. Website Brief Context

**Source**: website-post-onboarding-agent  
**Consumers**: Design team, copywriting team, development team  
**Extends**: Positioning context

```json
{
  "context_type": "website_brief",
  "generated_by": "website-post-onboarding-agent",
  "extends_positioning": true,
  "positioning_context": {...},
  
  "homepage_strategy": {
    "goal": "Communicate same-day reliability, address trust concerns, drive quote requests",
    
    "hero_section": {
      "headline": "Never Climb a Ladder Again",
      "subheadline": "Same-day gutter cleaning from a 20+ year expert. Licensed, insured, and backed by our lifetime guarantee.",
      "hero_image": "Before/after of gutter transformation",
      "primary_cta": {
        "text": "Get Your Free Inspection Today",
        "destination": "/schedule",
        "psychology": "Risk-free trial"
      },
      "secondary_cta": {
        "text": "See How We Work",
        "destination": "/process",
        "psychology": "Transparency building"
      }
    },
    
    "value_propositions": [
      {
        "pillar": "Same-Day Service",
        "icon": "speedometer",
        "headline": "Service Today, Worry Tomorrow",
        "copy": "Most calls completed within 24 hours. No waiting, no excuses.",
        "proof": "95% same-day/next-day completion rate"
      },
      {
        "pillar": "Local Expertise",
        "icon": "certified_badge",
        "headline": "20+ Years of Local Experience",
        "copy": "Founder-led service. We know Chicago gutters inside and out.",
        "proof": "Founder has 20+ years industry experience"
      },
      {
        "pillar": "Lifetime Guarantee",
        "icon": "shield",
        "headline": "Guaranteed Clog-Free",
        "copy": "If it clogs again during your ownership, we re-clean free. That's our guarantee.",
        "proof": "Unique market guarantee"
      }
    ],
    
    "social_proof_section": {
      "headline": "Trusted by 2,000+ Chicago Homeowners",
      "proof_elements": [
        "4.8★ on Google from 200+ reviews",
        "Customer testimonials (3-5 with photos)",
        "Before/after gallery (5-10 images)"
      ]
    },
    
    "final_cta_section": {
      "headline": "Ready to Stop Worrying About Your Gutters?",
      "copy": "Schedule a free inspection. No pressure, no sales pitch. Just honest assessment and transparent pricing.",
      "cta_button": "Book Your Free Inspection",
      "cta_psychology": "Risk-reversal + transparency"
    }
  },
  
  "recommended_sitemap": {
    "structure": [
      {
        "page": "Homepage",
        "purpose": "Problem → Solution → Trust → CTA",
        "flow": "Hook problem → Show solution → Build trust → Call to action"
      },
      {
        "page": "Services",
        "sub_pages": ["Gutter Cleaning", "Gutter Repair", "Downspout Services"],
        "purpose": "Detail offerings + pricing",
        "conversion_point": "Lead capture via quote request"
      },
      {
        "page": "Why Choose Us",
        "purpose": "Differentiators + proof points",
        "content": "Lifetime guarantee, same-day service, local expertise"
      },
      {
        "page": "Our Process",
        "purpose": "4-step process with visuals",
        "builds_trust": true
      },
      {
        "page": "Before & After Gallery",
        "purpose": "Visual proof of quality",
        "psychological_impact": "Demonstrates competence"
      },
      {
        "page": "Customer Testimonials",
        "purpose": "Social proof + emotional triggers",
        "content": "Real customer stories"
      },
      {
        "page": "Service Area Map",
        "purpose": "Coverage + local credibility",
        "builds_trust": true
      },
      {
        "page": "FAQ",
        "purpose": "Address objections",
        "sections": [
          "Why gutter cleaning matters",
          "Frequency recommendations",
          "Same-day capability",
          "Guarantee details",
          "Insurance coverage",
          "Pricing",
          "Service areas"
        ]
      },
      {
        "page": "Contact / Book Now",
        "purpose": "Multiple CTAs for lead capture",
        "contact_methods": ["Phone", "Form", "Booking system"]
      }
    ],
    
    "conversion_funnel": [
      "Homepage: 'I need this service'",
      "Services page: 'Do you handle my need + pricing?'",
      "Why Choose Us: 'Should I trust you?'",
      "Testimonials: 'What do others think?'",
      "Service Area: 'Do you serve my location?'",
      "Book/Contact: 'Let's schedule'"
    ]
  },
  
  "success_metrics": {
    "lead_volume": {
      "target": 15,
      "unit": "qualified leads per month",
      "baseline": "8-10 leads/month from Google Business + referrals",
      "success_threshold": "50% increase"
    },
    "conversion_rate": {
      "target": 0.20,
      "metric": "call-to-booking conversion",
      "baseline": "15% from word-of-mouth quality",
      "success_threshold": "Maintain or improve"
    },
    "customer_satisfaction": {
      "target": 4.8,
      "metric": "Google rating (stars)",
      "baseline": "4.8★ from 200+ reviews",
      "success_threshold": "Keep above 4.7★"
    },
    "service_area_expansion": {
      "target": "5+ new suburbs per quarter",
      "metric": "Service address locations",
      "baseline": "Primary core area only",
      "success_threshold": "Expand via website visibility"
    }
  }
}
```

---

## 3. Google Ads Research Context

**Source**: google-ads-research-agent  
**Consumers**: google-ads-strategy-agent, google-ads-landing-page-copywriter  
**Extends**: Positioning context

```json
{
  "context_type": "google_ads_research",
  "generated_by": "google-ads-research-agent",
  "extends_positioning": true,
  
  "competitor_analysis": [
    {
      "competitor_name": "Pro Gutter Pros",
      "positioning": "Speed/Convenience",
      "target_audience": "Busy professionals",
      "differentiators": ["Same-day service"],
      "price_range": "$150-300/visit",
      "ads_observed": ["Next-day gutter cleaning", "Fast, reliable service"],
      "gaps": "No mention of local expertise or guarantee"
    },
    {
      "competitor_name": "Local Gutters Co",
      "positioning": "Trust/Local presence",
      "target_audience": "Families",
      "differentiators": ["35+ years", "Family-owned"],
      "price_range": "$175-350/visit",
      "ads_observed": ["Family-owned since 1990", "Your local gutter experts"],
      "gaps": "No speed messaging"
    }
  ],
  
  "keyword_research": {
    "high_volume_keywords": [
      {
        "keyword": "gutter cleaning near me",
        "monthly_searches": 2400,
        "difficulty": "high",
        "intent": "Local service search"
      },
      {
        "keyword": "best gutter service chicago",
        "monthly_searches": 1200,
        "difficulty": "medium-high",
        "intent": "Local service search + quality"
      }
    ],
    "mid_volume_keywords": [
      {
        "keyword": "gutter cleaning same day",
        "monthly_searches": 450,
        "difficulty": "low",
        "intent": "Specific need matching positioning"
      }
    ],
    "low_competition_keywords": [
      {
        "keyword": "gutter cleaning guarantee",
        "monthly_searches": 85,
        "difficulty": "very_low",
        "intent": "Risk-reversal oriented"
      }
    ],
    "cpc_range": "$2-5"
  },
  
  "audience_insights": {
    "primary_intent": "Local service search with urgency",
    "primary_decision_criteria": [
      "Reviews (Google rating)",
      "Speed (same-day capability)",
      "Local presence",
      "Pricing transparency"
    ],
    "search_timing": [
      "Spring (gutters need cleaning after winter)",
      "Fall (gutters clogged with leaves)",
      "After storms (emergency gutter issues)"
    ],
    "device_behavior": {
      "mobile": "High (local searches + urgency)",
      "desktop": "Lower (research phase)"
    }
  },
  
  "ad_copy_angles": [
    {
      "angle": "Same-day guarantee",
      "hook": "Get your gutters cleaned TODAY",
      "proof": "95% of calls completed within 24 hours"
    },
    {
      "angle": "Local expert authority",
      "hook": "20+ years of Chicago gutter experience",
      "proof": "Founder-led, not franchised"
    },
    {
      "angle": "Risk reversal",
      "hook": "Guaranteed clog-free or we re-clean free",
      "proof": "Lifetime guarantee backs our work"
    },
    {
      "angle": "Professionalism",
      "hook": "Licensed, insured, professional team",
      "proof": "Full coverage for customer protection"
    }
  ],
  
  "budget_benchmarking": {
    "cost_per_click": "$2-5",
    "estimated_cost_per_lead": "$15-30",
    "estimated_lead_target": 15,
    "monthly_budget_for_target": "$225-450"
  }
}
```

---

## 4. SEO Research Context

**Source**: seo-research-agent  
**Consumers**: seo-content-planner-agent, seo-content-creator-agent  
**Extends**: Positioning context

```json
{
  "context_type": "seo_research",
  "generated_by": "seo-research-agent",
  "extends_positioning": true,
  
  "keyword_opportunities": [
    {
      "keyword": "gutter cleaning chicago",
      "monthly_searches": 1200,
      "difficulty": "moderate",
      "intent": "Local service search",
      "ranking_potential": "high",
      "recommended_content": "Homepage or services page"
    },
    {
      "keyword": "gutter maintenance tips",
      "monthly_searches": 450,
      "difficulty": "low",
      "intent": "Educational",
      "ranking_potential": "very_high",
      "recommended_content": "Blog post series"
    },
    {
      "keyword": "water damage prevention gutters",
      "monthly_searches": 320,
      "difficulty": "low",
      "intent": "Problem-focused",
      "ranking_potential": "high",
      "recommended_content": "Pillar content"
    }
  ],
  
  "topic_clusters": [
    {
      "pillar_page": "Gutter Cleaning Guide",
      "cluster_topic": "Understanding gutter maintenance",
      "supporting_content": [
        "When to clean gutters (seasonal guide)",
        "Signs your gutters need cleaning",
        "DIY vs professional gutter cleaning",
        "How often should you clean gutters"
      ]
    },
    {
      "pillar_page": "Water Damage Prevention",
      "cluster_topic": "Protecting your home",
      "supporting_content": [
        "Cost of water damage from neglected gutters",
        "Foundation damage prevention",
        "Siding and fascia protection"
      ]
    },
    {
      "pillar_page": "Gutter Types & Materials",
      "cluster_topic": "Gutter systems explained",
      "supporting_content": [
        "Aluminum vs copper gutters",
        "Gutter guards & covers",
        "Downspout options",
        "Gutter repair vs replacement"
      ]
    }
  ],
  
  "content_gaps": [
    {
      "gap": "No competitor ranks for 'water damage prevention'",
      "opportunity": "First-mover advantage in educational content"
    },
    {
      "gap": "Weak content on 'gutter protection systems'",
      "opportunity": "Detailed buyer's guide for gutter systems"
    },
    {
      "gap": "Missing local landing pages for suburbs",
      "opportunity": "Service-area-specific content pages"
    }
  ],
  
  "quick_wins": [
    {
      "win": "FAQ content",
      "ease": "Easy",
      "impact": "High",
      "rationale": "Site already has unaddressed questions"
    },
    {
      "win": "Seasonal maintenance guide",
      "ease": "Easy",
      "impact": "Medium",
      "rationale": "Seasonal high-intent search"
    }
  ]
}
```

---

## 5. Performance Context (Monthly Flow)

**Source**: Analytics, Google Ads, Search Console, conversion tracking  
**Consumers**: monthly-reporting-agent, cro-analysis-agent  
**Generated**: Monthly (Week 2 for reporting, Week 3 for CRO)

```json
{
  "context_type": "performance_data",
  "period": {
    "year": 2026,
    "month": "May",
    "start_date": "2026-05-01",
    "end_date": "2026-05-31"
  },
  
  "traffic_metrics": {
    "organic_sessions": 245,
    "organic_users": 198,
    "organic_conversion_rate": 0.12,
    "organic_revenue_per_user": "$42.50",
    
    "paid_sessions": 890,
    "paid_users": 752,
    "paid_conversion_rate": 0.18,
    "paid_cost_per_acquisition": "$28.50",
    
    "total_sessions": 1135,
    "total_conversions": 204
  },
  
  "conversion_data": {
    "total_leads_generated": 18,
    "qualified_leads": 14,
    "lead_quality_score": 0.78,
    "cost_per_lead": "$28.50",
    "booking_rate": 0.22,
    "booked_appointments": 4
  },
  
  "user_behavior": {
    "most_viewed_pages": [
      {
        "page": "/services/gutter-cleaning",
        "sessions": 156,
        "conversion_rate": 0.15,
        "avg_time_on_page": "2:34"
      },
      {
        "page": "/why-choose-us",
        "sessions": 98,
        "conversion_rate": 0.12
      }
    ],
    
    "highest_ctr_cta": "Get Free Inspection",
    "ctr_percentage": 0.24,
    
    "form_metrics": {
      "form_views": 120,
      "form_submissions": 82,
      "abandonment_rate": 0.32,
      "abandonment_trigger": "Long form with too many fields"
    },
    
    "scroll_depth": {
      "25_percent": 0.95,
      "50_percent": 0.78,
      "75_percent": 0.45,
      "100_percent": 0.22
    }
  },
  
  "paid_ads_performance": {
    "campaigns": [
      {
        "campaign_name": "Gutter Cleaning Brand",
        "spend": "$185",
        "clicks": 28,
        "cpc": "$6.60",
        "conversions": 5,
        "cpa": "$37",
        "roas": 2.4
      }
    ],
    "quality_score_avg": 6.5,
    "impression_share": 0.62,
    "lost_impression_share_budget": 0.28
  },
  
  "seo_performance": {
    "keywords_tracking": 24,
    "ranking_positions": {
      "position_1_3": 4,
      "position_4_10": 8,
      "position_11_20": 7,
      "position_21_plus": 5
    },
    "keywords_gaining": 3,
    "keywords_losing": 2
  },
  
  "bottlenecks": [
    {
      "bottleneck": "Contact form has high abandonment",
      "impact": "32% of interested users don't convert to lead",
      "cause": "Too many fields requested",
      "recommendation": "Reduce to 3-field form (name, phone, email)"
    },
    {
      "bottleneck": "Services page needs more detail",
      "impact": "Users leaving without understanding offerings",
      "cause": "Copy too brief",
      "recommendation": "Add service-specific landing pages"
    },
    {
      "bottleneck": "Mobile experience could be better",
      "impact": "Lower conversion on mobile vs desktop",
      "cause": "CTA button hard to tap",
      "recommendation": "Increase CTA button size and prominence on mobile"
    }
  ],
  
  "trends": {
    "traffic_trend": "up 12% from April",
    "conversion_trend": "flat (expected, new website)",
    "lead_quality_trend": "up (better targeting)",
    "cost_per_lead_trend": "down 8% from April"
  }
}
```

---

## 6. Content Creation Context (Monthly)

**Source**: Content calendar + previous month's performance  
**Used by**: seo-content-creator-agent  
**Generated**: Monthly (Week 1)

```json
{
  "context_type": "monthly_content_plan",
  "period": {
    "year": 2026,
    "month": "June",
    "content_count": 5,
    "total_word_target": 8000
  },
  
  "content_calendar": [
    {
      "article_number": 1,
      "topic": "When to Clean Your Gutters: A Seasonal Guide",
      "target_keyword": "when to clean gutters",
      "type": "Educational",
      "word_count": 1600,
      "outline": [
        "Why seasonal cleaning matters",
        "Spring cleaning (post-winter prep)",
        "Fall cleaning (leaf season)",
        "Storm season maintenance",
        "Signs your gutters need cleaning NOW"
      ],
      "internal_links": [
        "Link to: Water damage prevention page",
        "Link to: Gutter types page"
      ]
    },
    {
      "article_number": 2,
      "topic": "DIY Gutter Cleaning vs Professional Service: The Real Costs",
      "target_keyword": "diy gutter cleaning vs professional",
      "type": "Comparison",
      "word_count": 1400,
      "outline": [
        "Cost breakdown: DIY vs professional",
        "Safety considerations",
        "Time investment (your time value)",
        "Quality differences",
        "When DIY makes sense (and when it doesn't)"
      ]
    }
  ],
  
  "previous_month_insights": {
    "top_performing_topic": "Water damage prevention",
    "top_performing_ctr": 0.18,
    "keywords_that_gained": ["water damage gutters", "gutter maintenance"],
    "keywords_that_lost": ["residential gutters"],
    "user_intent_patterns": "Problem-focused content outperforms how-to"
  }
}
```

---

## Data Flow Diagram

```
┌─────────────────────────────┐
│ Positioning Context         │
│ (Approved at Gate 1)        │
└────────────┬────────────────┘
             │
      ┌──────┼──────┐
      │      │      │
      ▼      ▼      ▼
   [Copy] [Ads]  [SEO]
      │      │      │
      ▼      ▼      ▼
   [Brief][Ads Research] [SEO Research]
      │      │              │
      │      ▼              ▼
      │   [Ads Strategy][Content Plan]
      │      │              │
      │      ▼              ▼
      │   [Landing Page][Content Creator]
      │   [Copy]            │
      └─────┬───────────────┤
            │               │
            ▼               ▼
        [Design &      [Monthly Reporting]
         Development]      │
            │               ▼
            │          [CRO Analysis]
            ▼               │
        [Launch]            └─→ (Loop back to content creator)
            │
            ▼
        [Performance Data] ──┐
                             │
                             ▼
                        [Monthly Reporting]
                             │
                             ▼
                        [CRO Analysis]
```

---

## Context Validation Rules

Before invoking downstream skill, validate:

1. **Positioning context exists** and is approved (required by ALL skills)
2. **Required context fields** are non-null and properly formatted
3. **Data types match** expected types (string vs array vs object)
4. **Timestamps are recent** (not stale data)
5. **Approval gates cleared** (if context depends on approval)

**Validation failure**: Loop back to upstream skill with adjusted input
