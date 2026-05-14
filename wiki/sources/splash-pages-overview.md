# Splash Pages & Launch Screens: Authoritative Sources Overview

## Summary

This page synthesizes the key authoritative resources on product splash pages (web) and mobile app launch screens. The sources span research-backed usability guidance (NN/g), official platform guidelines (Apple, Android/Material Design), and practitioner analysis (Smashing Magazine, Eleken). The consensus across sources is that splash pages carry high friction costs and should be avoided on the web unless legally mandated, while mobile launch screens are a required, tightly constrained system component focused entirely on perceived performance.

## Key Takeaways

- **NN/g**: Splash pages are among the most hated web design elements; avoid unless legally required (age verification, cookie consent, region selection). Prioritize giving users immediate value.
- **Smashing Magazine (2007, still canonical)**: Documents ~12 legitimate purposes but recommends against use in most cases due to load time, navigation loss, and user abandonment.
- **Apple HIG**: iOS/iPadOS/tvOS require a launch screen that must look nearly identical to the app's first screen — sole purpose is masking load time, not branding.
- **Android/Material Design**: Android 12+ uses system-managed splash screens with strict icon/color specs. Purpose is brand continuity during initialization, not engagement.
- **Eleken (2026)**: Practical guide for web use cases — single CTA, fast load, brand-consistent, mobile-first, SEO-safe (avoid blocking root URL for crawlers), personalized via geo/cookies.

## Origins/History

The web splash page emerged in the late 1990s alongside Flash-based "intro" animations, often used to set visual tone before entering a site. Their reputation declined rapidly as usability research showed users bypassed or abandoned them. Mobile app launch screens evolved separately, driven by OS-level loading mechanics. Apple formalized launch screen requirements with iOS guidelines; Android followed with system-managed splash screens in Android 12 (2021), eliminating developer inconsistency.

## Applications

- **Web/product**: Age gates, country/language selectors, promo or hype screens, audience segmentation, legal disclaimers (cookies, age).
- **Mobile native apps**: iOS/iPadOS/tvOS launch screens (required), optional onboarding splash for first-run flows.
- **Decision framework**: Default to no splash on web; follow platform mandates on mobile; A/B test and monitor bounce rates when in doubt.

## See Also

- [Splash Screens (topic)](../topics/splash-screens.md)
- [Apple HIG: Platform Guidelines](./apple-hig-platform-guidelines.md)
- [Apple HIG: UI Elements](./apple-hig-ui-elements.md)
- [Material Design Overview](./material-design-overview.md)
- [NN/g: 10 Usability Heuristics](./nn-g-10-usability-heuristics.md)

## Sources

- [Splash Pages Reference](../../raw/splash-pages/splash-pages-reference.md)
- NN/g: https://www.nngroup.com/articles/homepage-design-principles/
- Smashing Magazine: https://www.smashingmagazine.com/2007/10/splash-pages-do-we-really-need-them/
- Apple HIG Launching: https://developer.apple.com/design/human-interface-guidelines/launching
- Android Splash: https://developer.android.com/develop/ui/views/launch/splash-screen
- Material Design Launch: https://m2.material.io/design/communication/launch-screen.html
- Eleken: https://www.eleken.co/blog-posts/what-are-splash-pages-15-inspiring-examples-and-best-practices
