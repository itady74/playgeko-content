# PlayGeko — Technical SEO + Schema Markup

> Last updated: 2026-08-29
> Purpose: On-page SEO blueprint, schema implementation guide, metadata specs.

---

## Site-Wide Technical Requirements

### URL Structure
- Protocol: HTTPS only
- Trailing slash: No (canonical = no trailing slash)
- www: Redirect www → non-www (or vice versa, pick one)
- Case: Lowercase only
- Parameters: Minimize; block tracking params in robots.txt

### Canonical Tags
- Every page must have `<link rel="canonical" href="..." />`
- Self-referencing canonicals on all pages
- Match the URL in the sitemap exactly

### Open Graph & Twitter Cards
```html
<!-- Open Graph -->
<meta property="og:type" content="website" />
<meta property="og:title" content="[Page Title] | PlayGeko" />
<meta property="og:description" content="[Meta Description]" />
<meta property="og:image" content="https://www.playgeko.com/static/og/[page].png" />
<meta property="og:url" content="https://www.playgeko.com/[page]" />
<meta property="og:site_name" content="PlayGeko" />

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="[Page Title] | PlayGeko" />
<meta name="twitter:description" content="[Meta Description]" />
<meta name="twitter:image" content="https://www.playgeko.com/static/og/[page].png" />
```

### Core Web Vitals Targets
| Metric | Target | Tool |
|--------|--------|------|
| LCP | < 2.5s | Lighthouse |
| FID | < 100ms | Lighthouse |
| CLS | < 0.1 | Lighthouse |
| TTFB | < 800ms | Lighthouse |
| INP | < 200ms | Lighthouse |

### Image Optimization
- Format: WebP with JPEG fallback
- Alt text: Descriptive, include keyword naturally
- Lazy loading: Yes, below-fold images
- Dimensions: Specify width/height to prevent CLS
- Compress: < 200KB for most images

### Mobile
- Responsive design (Google mobile-first indexing)
- No horizontal scroll
- Touch targets: min 48x48px
- Font size: min 16px body text

---

## Per-Page SEO Metadata

### Homepage (`/`)
```yaml
title: "PlayGeko — Club Management Software for Padel, Tennis & Squash"
meta_description: "Manage court bookings, payments, coaching, leagues, and tournaments from one dashboard. Built for padel, tennis, squash, and multi-sport clubs."
h1: "The Platform That Runs Your Entire Club."
canonical: "https://www.playgeko.com/"
og_title: "PlayGeko — Club Management Software"
og_description: "Court bookings, CRM, POS, coaching, leagues, and tournaments — in one platform."
og_image: "https://www.playgeko.com/static/og/home.png"
```

### Features (`/features`)
```yaml
title: "Club Management Software Features | Court Booking, CRM, POS | PlayGeko"
meta_description: "PlayGeko manages court bookings, payments, coaching, leagues, and tournaments for padel, tennis, and squash clubs. One dashboard. Total control."
h1: "Everything Your Club Needs. Nothing It Doesn't."
canonical: "https://www.playgeko.com/features"
og_title: "PlayGeko Features — Club Management Software"
og_description: "Court booking, CRM, POS, coaching, leagues, tournaments, and AI insights — all in one platform."
og_image: "https://www.playgeko.com/static/og/features.png"
```

### How It Works (`/how-it-works`)
```yaml
title: "How PlayGeko Works | Set Up Your Club in 10 Minutes"
meta_description: "Sign up, add your courts, invite your team, and start taking bookings. No contracts, no IT team required."
h1: "Up and Running in 10 Minutes. Seriously."
canonical: "https://www.playgeko.com/how-it-works"
og_title: "How PlayGeko Works"
og_description: "Sign up, add courts, start booking. Setup takes 10 minutes."
og_image: "https://www.playgeko.com/static/og/how-it-works.png"
```

### Pricing (`/pricing`)
```yaml
title: "PlayGeko Pricing | Club Management Software Plans"
meta_description: "Simple, transparent pricing. Standard from $40/mo. Professional from $94/mo. Custom plans available. Start free trial."
h1: "Pricing That Grows With Your Club."
canonical: "https://www.playgeko.com/pricing"
og_title: "PlayGeko Pricing"
og_description: "From $40/mo. Free trial. No contracts."
og_image: "https://www.playgeko.com/static/og/pricing.png"
```

### Padel (`/padel`)
```yaml
title: "Padel Club Management Software | Court Booking & Operations | PlayGeko"
meta_description: "Software built specifically for padel clubs. Court booking, league management, coaching packages, and tournaments. Padel is growing 40% YoY."
h1: "Software Built for Padel Clubs."
canonical: "https://www.playgeko.com/padel"
og_title: "Padel Club Management Software — PlayGeko"
og_description: "Court booking, leagues, coaching, and tournaments for padel clubs."
og_image: "https://www.playgeko.com/static/og/padel.png"
```

### Tennis (`/tennis`)
```yaml
title: "Tennis Club Management Software | Court Booking & Coaching | PlayGeko"
meta_description: "Tennis club software that handles court scheduling, lessons, memberships, and leagues. From single courts to multi-location facilities."
h1: "Tennis Club Management, Simplified."
canonical: "https://www.playgeko.com/tennis"
og_title: "Tennis Club Management Software — PlayGeko"
og_description: "Court scheduling, lessons, memberships, and leagues for tennis clubs."
og_image: "https://www.playgeko.com/static/og/tennis.png"
```

### Squash (`/squash`)
```yaml
title: "Squash Court Booking Software | Club Management | PlayGeko"
meta_description: "Squash court scheduling, league play, and club management. Simple software for squash facilities."
h1: "Squash Club Operations, Handled."
canonical: "https://www.playgeko.com/squash"
og_title: "Squash Club Management Software — PlayGeko"
og_description: "Court scheduling, leagues, and coaching for squash clubs."
og_image: "https://www.playgeko.com/static/og/squash.png"
```

### Multi-Sport (`/multi-sport`)
```yaml
title: "Multi-Sport Facility Management Software | PlayGeko"
meta_description: "One platform for every sport, every court, every booking. Manage padel, tennis, squash, and more from a single dashboard."
h1: "One Platform. Every Sport."
canonical: "https://www.playgeko.com/multi-sport"
og_title: "Multi-Sport Facility Management — PlayGeko"
og_description: "Manage multiple sports from one platform."
og_image: "https://www.playgeko.com/static/og/multi-sport.png"
```

### Basketball (`/basketball`)
```yaml
title: "Basketball Court Booking Software | Facility Management | PlayGeko"
meta_description: "Book basketball courts, manage teams, and run leagues. Software for indoor basketball facilities."
h1: "Basketball Court Management Made Simple."
canonical: "https://www.playgeko.com/basketball"
og_title: "Basketball Court Management — PlayGeko"
og_description: "Court booking and team management for basketball facilities."
og_image: "https://www.playgeko.com/static/og/basketball.png"
```

### Handball (`/handball`)
```yaml
title: "Handball Club Management Software | Court Booking | PlayGeko"
meta_description: "Handball court scheduling, team management, and tournament brackets. Streamlined operations for handball clubs."
h1: "Handball Club Operations, Streamlined."
canonical: "https://www.playgeko.com/handball"
og_title: "Handball Club Management — PlayGeko"
og_description: "Court booking and tournament management for handball clubs."
og_image: "https://www.playgeko.com/static/og/handball.png"
```

### AI Features (`/ai`)
```yaml
title: "AI-Powered Club Management | Smart Recommendations | PlayGeko"
meta_description: "PlayGeko uses AI to recommend optimal booking times, predict member churn, and suggest pricing adjustments. Smart growth, not just software."
h1: "Smart Recommendations. Not Just Software."
canonical: "https://www.playgeko.com/ai"
og_title: "AI Club Management — PlayGeko"
og_description: "AI-powered insights for bookings, revenue, and member engagement."
og_image: "https://www.playgeko.com/static/og/ai.png"
```

### Case Studies (`/case-studies`)
```yaml
title: "Club Management Case Studies | Success Stories | PlayGeko"
meta_description: "See how clubs use PlayGeko to manage courts, grow membership, and streamline operations. Real results from real clubs."
h1: "Real Clubs. Real Results."
canonical: "https://www.playgeko.com/case-studies"
og_title: "PlayGeko Case Studies"
og_description: "How clubs use PlayGeko to grow."
og_image: "https://www.playgeko.com/static/og/case-studies.png"
```

---

## Schema Markup (JSON-LD)

### Site-Wide Schema (Homepage — appears on all pages via template)

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "@id": "https://www.playgeko.com/#organization",
      "name": "PlayGeko",
      "url": "https://www.playgeko.com",
      "logo": {
        "@type": "ImageObject",
        "url": "https://www.playgeko.com/static/logo.png",
        "width": 384,
        "height": 120
      },
      "description": "The all-in-one club management platform for padel, tennis, squash, and multi-sport facilities.",
      "sameAs": [
        "https://www.instagram.com/getplaygeko/",
        "https://www.linkedin.com/company/playgeko/"
      ],
      "contactPoint": {
        "@type": "ContactPoint",
        "contactType": "customer service",
        "email": "hello@playgeko.com",
        "availableLanguage": ["English", "Arabic", "French"]
      },
      "areaServed": "Worldwide",
      "founder": {
        "@type": "Person",
        "@id": "https://www.playgeko.com/#founder",
        "name": "[Founder Name]",
        "jobTitle": "Founder",
        "worksFor": {
          "@id": "https://www.playgeko.com/#organization"
        }
      }
    },
    {
      "@type": "WebSite",
      "@id": "https://www.playgeko.com/#website",
      "url": "https://www.playgeko.com",
      "name": "PlayGeko",
      "publisher": {
        "@id": "https://www.playgeko.com/#organization"
      },
      "potentialAction": {
        "@type": "SearchAction",
        "target": "https://www.playgeko.com/search?q={search_term_string}",
        "query-input": "required name=search_term_string"
      }
    }
  ]
}
```

### Features Page Schema

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Product",
      "@id": "https://www.playgeko.com/features/#product",
      "name": "PlayGeko Club Management Platform",
      "description": "All-in-one club management software for court booking, CRM, POS, coaching, leagues, and tournaments.",
      "brand": {
        "@id": "https://www.playgeko.com/#organization"
      },
      "url": "https://www.playgeko.com/features",
      "offers": [
        {
          "@type": "Offer",
          "name": "Standard",
          "price": "40",
          "priceCurrency": "USD",
          "priceSpecification": {
            "@type": "UnitPriceSpecification",
            "price": "40",
            "priceCurrency": "USD",
            "billingDuration": "P1M"
          },
          "availability": "https://schema.org/InStock"
        },
        {
          "@type": "Offer",
          "name": "Professional",
          "price": "94",
          "priceCurrency": "USD",
          "priceSpecification": {
            "@type": "UnitPriceSpecification",
            "price": "94",
            "priceCurrency": "USD",
            "billingDuration": "P1M"
          },
          "availability": "https://schema.org/InStock"
        }
      ]
    },
    {
      "@type": "FAQPage",
      "@id": "https://www.playgeko.com/features/#faq",
      "mainEntity": [
        {
          "@type": "Question",
          "name": "What features does PlayGeko include?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "PlayGeko includes court booking, CRM, payments, POS, coaching management, leagues, tournaments, a white-label mobile app, and AI-driven analytics."
          }
        },
        {
          "@type": "Question",
          "name": "Can I manage multiple sports on PlayGeko?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Yes. PlayGeko supports padel, tennis, squash, basketball, handball, and other court-based sports from a single dashboard."
          }
        },
        {
          "@type": "Question",
          "name": "Does PlayGeko offer a white-label app?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Yes. The Custom plan includes a white-label mobile app with your club's branding, available on iOS and Android."
          }
        }
      ]
    }
  ]
}
```

### How It Works Schema

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "How to Set Up PlayGeko for Your Club",
  "description": "Set up your club on PlayGeko in 10 minutes. No technical skills required.",
  "step": [
    {
      "@type": "HowToStep",
      "name": "Create Your Club",
      "text": "Sign up, enter your club name, add your sports and courts, and set your pricing.",
      "url": "https://www.playgeko.com/how-it-works#step-1"
    },
    {
      "@type": "HowToStep",
      "name": "Invite Your Team",
      "text": "Add staff members, assign roles and permissions, and configure access levels.",
      "url": "https://www.playgeko.com/how-it-works#step-2"
    },
    {
      "@type": "HowToStep",
      "name": "Start Taking Bookings",
      "text": "Players download your app, browse available courts, book and pay online. You manage everything from the dashboard.",
      "url": "https://www.playgeko.com/how-it-works#step-3"
    }
  ]
}
```

### Industry Page Schema (Padel Example)

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Article",
      "@id": "https://www.playgeko.com/padel/#article",
      "headline": "Software Built for Padel Clubs",
      "description": "PlayGeko is club management software built specifically for padel operations — court booking, leagues, coaching, and tournaments.",
      "author": {
        "@id": "https://www.playgeko.com/#founder"
      },
      "publisher": {
        "@id": "https://www.playgeko.com/#organization"
      },
      "datePublished": "2026-08-29",
      "dateModified": "2026-08-29",
      "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://www.playgeko.com/padel"
      },
      "about": {
        "@type": "Thing",
        "name": "Padel Club Management"
      }
    },
    {
      "@type": "FAQPage",
      "@id": "https://www.playgeko.com/padel/#faq",
      "mainEntity": [
        {
          "@type": "Question",
          "name": "What software do padel clubs use?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Padel clubs use club management software like PlayGeko to handle court bookings, member management, league organization, coaching sessions, and payment processing."
          }
        },
        {
          "@type": "Question",
          "name": "How do I manage padel court bookings?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Use a court booking system that shows real-time availability, handles group bookings, and sends automated reminders. PlayGeko provides all of this with zero double-bookings."
          }
        },
        {
          "@type": "Question",
          "name": "Can I run padel tournaments with PlayGeko?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Yes. PlayGeko handles bracket generation, scheduling, court assignments, and results tracking for padel tournaments end-to-end."
          }
        }
      ]
    }
  ]
}
```

### Pricing Page Schema

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Product",
      "@id": "https://www.playgeko.com/pricing/#standard",
      "name": "PlayGeko Standard",
      "description": "For clubs going digital for the first time. 1 branch, 3 courts, 1 staff seat.",
      "brand": {
        "@id": "https://www.playgeko.com/#organization"
      },
      "offers": {
        "@type": "Offer",
        "price": "40",
        "priceCurrency": "USD",
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "40",
          "priceCurrency": "USD",
          "billingDuration": "P1M"
        },
        "availability": "https://schema.org/InStock",
        "url": "https://admin.playgeko.com/sign-up"
      }
    },
    {
      "@type": "Product",
      "@id": "https://www.playgeko.com/pricing/#professional",
      "name": "PlayGeko Professional",
      "description": "For clubs running real operations. Up to 5 branches, 10 courts, 4 staff seats.",
      "brand": {
        "@id": "https://www.playgeko.com/#organization"
      },
      "offers": {
        "@type": "Offer",
        "price": "94",
        "priceCurrency": "USD",
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "94",
          "priceCurrency": "USD",
          "billingDuration": "P1M"
        },
        "availability": "https://schema.org/InStock",
        "url": "https://admin.playgeko.com/sign-up"
      }
    }
  ]
}
```

---

## Internal Linking Map

| From | To (priority links) |
|------|---------------------|
| Homepage | /features, /pricing, /padel, /tennis, /how-it-works |
| Features | /how-it-works, /pricing, /ai, /padel |
| How It Works | /features, /pricing |
| Pricing | /features, /how-it-works |
| Padel | /features, /tennis, /case-studies |
| Tennis | /features, /padel, /case-studies |
| Squash | /features, /multi-sport |
| Multi-Sport | /features, /padel, /tennis |
| Basketball | /features, /multi-sport |
| Handball | /features, /multi-sport |
| AI Features | /features, /case-studies |
| Case Studies | /features, /padel, /tennis, /pricing |

---

## Validation Checklist

- [ ] All pages have unique title tag (50-60 chars)
- [ ] All pages have unique meta description (150-160 chars)
- [ ] All pages have H1 (one per page)
- [ ] All pages have canonical tag
- [ ] All pages have Open Graph tags
- [ ] Schema validates at schema.org/validator
- [ ] Schema validates at Google Rich Results Test
- [ ] All images have alt text
- [ ] No duplicate content across pages
- [ ] Internal links use consistent URL format
- [ ] XML sitemap matches actual canonical URLs
- [ ] robots.txt doesn't block any public page
- [ ] Mobile-responsive on all pages
- [ ] Core Web Vitals pass on all pages
