# Splash Screens & Launch Screens

## Summary

A splash screen is a transitional screen shown to users at the moment a product is first encountered — either when entering a website (web splash page) or when opening a mobile app (launch screen). Despite sharing the name, these two contexts have fundamentally different purposes, constraints, and best practices. Web splash pages are largely a UX anti-pattern reserved for legal or segmentation needs; mobile launch screens are platform-required loading masks governed by strict OS guidelines.

The overarching principle across both: **the faster users reach real content or functionality, the better.**

## Key Takeaways

- Web splash pages introduce friction before users see value — NN/g research identifies them among the most disliked web design elements.
- The only defensible web splash page use cases are legally mandated or functionally necessary: age verification, country/language selection, cookie consent, legal disclaimers.
- Mobile app launch screens are required on iOS/iPadOS/tvOS and are system-managed on Android 12+; their sole purpose is masking load time.
- Apple HIG mandates that launch screens look nearly identical to the app's first screen — no branding embellishment, no animations, no logo-as-identity play.
- The 3-second rule applies broadly: any splash lasting more than 2–3 seconds damages perceived performance; daily-use apps should aim under 1 second.
- SEO risk: a splash page at the root URL can block search crawler access to indexable content; use subdirectory or modal patterns instead.

## Origins/History

Web splash pages emerged in the late 1990s with Flash-based intro animations — decorative experiences that set visual tone before revealing a site. User research rapidly undermined their reputation: bounce rates increased, and polls showed strong preference against them. Usability publications like NN/g and Smashing Magazine documented their decline through the 2000s.

Mobile launch screens arose separately, shaped by OS-level loading mechanics. With iOS, Apple required launch screens as a performance-perception mechanism — devices needed time to load the app into memory, and a static screen prevented a blank flash. Android introduced formal splash screen APIs in Android 12 (2021), systematizing what had previously been ad-hoc developer implementations.

## Applications

### Web Splash Pages — When to Use

Use sparingly and only for:

| Use Case | Rationale |
|---|---|
| Age verification | Legal requirement (alcohol, gambling, adult content) |
| Country/region selector | Redirects to localized content (e.g., IKEA) |
| Language selection | Applicable when geo-IP is unreliable |
| Cookie/privacy consent | GDPR/CCPA legal obligation |
| Audience segmentation | Directing user types to different product areas |
| Pre-launch hype | One-time use; requires clear countdown/CTA |

**Never use for**: Generic branding intros, promotional upsells, or any content that could be shown inline.

### Web Splash Page Design Rules

- **Single CTA only** — one clear action (Enter, Select Country, Verify Age). No navigation.
- **Fast load** — lightweight assets; no blocking resources. Users already waiting to enter.
- **Easy exit** — provide skip where legally permissible; never trap users.
- **SEO-safe** — don't block root URL from crawlers. Use modal overlays or `/splash` subdirectory patterns.
- **Mobile-first** — full-screen, touch-friendly, responsive.
- **Brand-consistent** — match primary color palette and typography; users should feel continuity.
- **Personalize** — use geo or cookie data to pre-select country/language where possible; minimize friction.
- **A/B test** — monitor bounce rates, time-to-enter, and conversions; kill what underperforms.

### Mobile App Launch Screens (iOS)

Apple HIG rules for iOS/iPadOS/tvOS:

- Launch screen is **required** — appears instantly while the OS loads the app.
- Must be **visually identical to the first screen** of the app: same background color, same layout skeleton (no placeholder content). Mismatch causes a disorienting "flash."
- **No logos, no text, no animations** — the launch screen is not a branding moment. It is a perceived-performance mechanism.
- Replaced immediately once app is ready. Duration is loading time, not a design choice.
- macOS, watchOS, and visionOS generally do not require launch screens.

### Mobile App Launch Screens (Android)

Android 12+ guidelines:

- System-managed: developers customize via `windowSplashScreenBackground`, `windowSplashScreenAnimatedIcon`, and `windowSplashScreenIconBackgroundColor`.
- Icon spec: 432 dp animated area; standard or adaptive icon format.
- Supports day/night mode via theme attributes.
- Animated vector drawables supported for icon animation (up to 1000ms).
- Smooth exit animation to app's first activity.
- Rationale: provide brand continuity during cold start; eliminate blank screens.

### Mobile App Optional Splash (Onboarding Context)

For first-run onboarding flows, a brief branded splash is acceptable on both platforms:
- Duration: ideally ≤2 seconds; maximum 3 seconds.
- For daily-use apps (email, social): target ≤1 second — users expect immediacy.
- Simple, elegant animation preferred over static image.
- Should feel like a natural transition into the onboarding or main experience.

## Common Failure Modes

- **Promotional modals stacked on splash**: violates user trust; NN/g lists as top hated pattern.
- **Forced new window**: traps users; violates user control heuristic.
- **Flash mismatch (mobile)**: launch screen background/layout differs from app's first screen, causing jarring visual jump.
- **Logo-as-launch-screen**: common anti-pattern on iOS; Apple HIG explicitly discourages branding-focused launch screens.
- **Root URL splash with no fallback**: SEO crawler cannot index site content; search ranking suffers.
- **Duration creep**: artificial delays to "show" the splash longer than loading requires — never do this.

## See Also

- [Splash Pages Overview (sources)](../sources/splash-pages-overview.md)
- [Apple HIG: Platform Guidelines](../sources/apple-hig-platform-guidelines.md)
- [Material Design Overview](../sources/material-design-overview.md)
- [Onboarding Flows](./onboarding-flows.md)
- [10 Usability Heuristics](../concepts/10-usability-heuristics.md)

## Sources

- [Splash Pages Reference (raw)](../../raw/splash-pages/splash-pages-reference.md)
- NN/g Homepage Design Principles: https://www.nngroup.com/articles/homepage-design-principles/
- Smashing Magazine — Sven Lennartz (2007): https://www.smashingmagazine.com/2007/10/splash-pages-do-we-really-need-them/
- Apple HIG Launching: https://developer.apple.com/design/human-interface-guidelines/launching
- Android Splash Screen API: https://developer.android.com/develop/ui/views/launch/splash-screen
- Material Design Launch Screen: https://m2.material.io/design/communication/launch-screen.html
- Eleken (2026): https://www.eleken.co/blog-posts/what-are-splash-pages-15-inspiring-examples-and-best-practices
