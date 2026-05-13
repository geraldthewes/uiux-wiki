# Web Typography

## Summary
Web typography encompasses the specific considerations, techniques, and technologies for implementing type on digital screens. It addresses the unique challenges of rendering text across various devices, resolutions, and browsers while maintaining readability, performance, and accessibility.

## Core Challenges of Web Typography

### 1. Rendering Variability
- **Different Operating Systems**: Windows, macOS, Linux, iOS, Android each render type differently
- **Browser Variations**: Chrome, Firefox, Safari, Edge have subtle rendering differences
- **Screen Resolutions**: From low-DPI monitors to high-DPI Retina/4K displays
- **Color Management**: Different color profiles and gamma settings affect perceived appearance

### 2. Performance Considerations
- **Font File Sizes**: Web fonts can significantly impact page load times
- **Render Blocking**: CSS and fonts can delay text rendering
- **Layout Shifts**: Font loading can cause content to reflow (CLS - Cumulative Layout Shift)
- **Network Conditions**: Users on slow connections experience delayed typography

### 3. Accessibility Requirements
- **Scalability**: Text must remain readable when resized up to 200%
- **Contrast**: Sufficient foreground/background contrast required
- **Preference Respect**: Honoring user preferences for reduced motion, increased contrast, etc.
- **Assistive Technology Compatibility**: Working with screen readers, zoom tools, etc.

### 4. Internationalization and Localization
- **Character Sets**: Supporting diverse scripts and languages
- **Directionality**: Handling left-to-right and right-to-left layouts
- **Typography Traditions**: Respecting language-specific typesetting conventions
- **Fallback Systems**: Ensuring readability when preferred fonts aren't available

## Web Font Technologies

### 1. Font Formats
#### WOFF2 (Web Open Font Format 2)
- **Current Standard**: Best compression and broad browser support
- **Typical Savings**: 30% better compression than WOFF
- **Support**: All modern browsers (Chrome, Firefox, Safari, Edge)
- **Use Case**: Primary format for web fonts

#### WOFF (Web Open Font Format)
- **Legacy Format**: Still useful for older browser support
- **Compression**: Good but not as efficient as WOFF2
- **Support**: IE9+, all modern browsers
- **Use Case**: Fallback for older browsers when needed

#### TTF/OTF (TrueType/OpenType)
- **Desktop Formats**: Not recommended for web use due to lack of compression
- **Licensing**: Often restricted for web embedding
- **Use Case**: Development/testing only; convert to WOFF/WOFF2 for production

#### EOT (Embedded OpenType)
- **Legacy IE Format**: Primarily for IE8 and older
- **Compression**: Similar to WOFF but with DRM features
- **Support**: IE8 only
- **Use Case**: Generally obsolete; only needed for very old IE support

#### SVG Fonts
- **Deprecated**: Removed from most browsers due to security and performance issues
- **Use Case**: Avoid entirely

### 2. Variable Fonts
#### Advantages
- **Single File**: Contains multiple variations (weight, width, slant, etc.) in one file
- **Reduced Requests**: Fewer font files to load
- **Fine-Grained Control**: Access to intermediate values not available in static fonts
- **Animation Potential**: Smooth transitions between variations
- **Future-Proof**: Can contain static font instances as fallback

#### Axes of Variation
- **wght (Weight)**: Range from thin to black (typically 100-900)
- **wdth (Width)**: Range from ultra-condensed to ultra-expanded
- **slnt (Slant)**: Angle of slant for oblique styles
- **ital (Italic)**: Binary switch for true italic vs oblique
- **opsz (Optical Size)**: Different designs for different sizes
- **GRAN, XOPQ, etc.**: Custom axes for specific typeface features

#### Browser Support
- **Excellent**: Chrome, Firefox, Safari, Edge all support variable fonts
- **Considerations**: Some older mobile browsers may have limited support
- **Fallback Strategy**: Use @supports to detect variable font capability

### 3. Font Loading Strategies
#### Critical FOFT (Flash of Faux Text)
- **Approach**: Load essential fonts first, use system fonts initially
- **Benefit**: Fast initial render, minimal layout shift
- **Implementation**: 
  ```css
  /* Load critical fonts in head */
  <link rel="preload" as="font" href="/fonts/raleway-v20-latin-regular.woff2" type="font/woff2" crossorigin>
  ```

#### FOIT (Flash of Invisible Text) vs FOUT (Flash of Unstyled Text)
- **FOIT**: Browser hides text until font loads (can cause blank text)
- **FOUT**: Browser shows fallback font immediately (can cause jarring shift)
- **Preferred**: FOUT is generally better for perceived performance

#### font-display Property
```css
@font-face {
  font-family: 'MyFont';
  src: url('myfont.woff2') format('woff2');
  font-display: swap; /* Options: auto, block, swap, fallback, optional */
}
```
- **auto**: Browser default (usually similar to block)
- **block**: Short block period (~100ms) then swap
- **swap**: Zero block period, immediate swap (recommended for body text)
- **fallback**: Very short block (~100ms) then swap with timeout
- **optional**: Extremely short block, font may not be used if slow

#### Preloading and Prefetching
```html
<!-- In document head -->
<link rel="preload" as="font" href="/fonts/font-name.woff2" type="font/woff2" crossorigin>
<link rel="prefetch" as="font" href("/fonts/font-name-bold.woff2")>
```

#### CSS Font Loading API
```javascript
// Advanced control over font loading
if ('fonts' in document) {
  document.fonts.load('1em MyFont')
    .then(() => {
      // Font is loaded, do something
      document.documentElement.classList.add('fonts-loaded');
    })
    .catch(() => {
      // Font failed to load
    });
}
```

## Implementation Best Practices

### 1. Font Selection and Preparation
#### Choosing Web-Friendly Fonts
- **License Compliance**: Ensure font license permits web embedding
- **Web Optimization**: Prefer fonts specifically optimized for web use
- **Character Coverage**: Verify needed characters, symbols, and languages are included
- **Hinting**: Look for well-hinted fonts for better screen rendering
- **File Size**: Consider impact on performance; subset when possible

#### Font Preparation Workflow
1. **Source**: Obtain licensed font files (OTF/TTF)
2. **Subset**: Remove unused characters to reduce file size
   - Tools: glyphhanger, pyftsubset, FontTools
3. **Convert**: Generate WOFF2 and WOFF formats
   - Tools: woff2_compress, sfnt2woff, Font Squirrel
4. **Optimize**: Consider variable fonts when appropriate
5. **Test**: Verify rendering across browsers and devices

### 2. CSS Implementation Patterns
#### Basic @font-face Declaration
```css
/* Primary font declaration */
@font-face {
  font-family: 'Inter';
  src: url('/fonts/inter-v12-latin-200.woff2') format('woff2');
  font-weight: 200;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Inter';
  src: url('/fonts/inter-v12-latin-300.woff2') format('woff2');
  font-weight: 300;
  font-style: normal;
  font-display: swap;
}

/* Repeat for other weights and styles */

/* Variable font example */
@font-face {
  font-family: 'InterVariable';
  src: url('/fonts/inter-variable-latin.woff2') format('woff2');
  font-weight: 100 900;
  font-display: swap;
}
```

#### Using System Font Stacks
```css
/* Optimized system font stack */
body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 
               Roboto, 'Helvetica Neue', Arial, 'Noto Sans', 
               sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 
               'Segoe UI Symbol', 'Noto Color Emoji';
}

/* Performance benefits: */
/* - Zero font loading delay */
/* - Perfect optical sizing on each platform */
/* - Familiar appearance to users */
/* - Automatic language support */
```

#### Modular Scale with CSS Custom Properties
```css
:root {
  /* Base measurements */
  --font-size-base: 1rem; /* 16px */
  --ratio: 1.25; /* Major third */
  
  /* Calculated sizes */
  --font-size-xs: calc(var(--font-size-base) / var(--ratio) / var(--ratio)); /* 0.64rem */
  --font-size-sm: calc(var(--font-size-base) / var(--ratio)); /* 0.8rem */
  --font-size-md: var(--font-size-base); /* 1rem */
  --font-size-lg: calc(var(--font-size-base) * var(--ratio)); /* 1.25rem */
  --font-size-xl: calc(var(--font-size-base) * var(--ratio) * var(--ratio)); /* 1.5625rem */
  
  /* Line heights */
  --line-height-tight: 1.2;
  --line-height-normal: 1.5;
  --line-height-loose: 1.8;
  
  /* Font weights */
  --font-weight-light: 300;
  --font-weight-regular: 400;
  --font-weight-medium: 500;
  --font-weight-semibold: 600;
  --font-weight-bold: 700;
  
  /* Font families */
  --font-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', 
               Roboto, 'Helvetica Neue', Arial, sans-serif;
  --font-serif: 'Merriweather', Georgia, 'Times New Roman', serif;
  --font-mono: 'Fira Code', 'Source Code Pro', Menlo, Monaco, monospace;
}

/* Usage */
h1 {
  font-family: var(--font-sans);
  font-size: var(--font-size-xl);
  font-weight: var(--font-weight-bold);
  line-height: var(--line-height-tight);
}

p {
  font-family: var(--font-sans);
  font-size: var(--font-size-md);
  font-weight: var(--font-weight-regular);
  line-height: var(--line-height-normal);
}
```

### 3. Performance Optimization Techniques
#### Font Loading Optimization
```css
/* Minimize repaints and layout shifts */
@font-face {
  font-family: 'Lato';
  src: url('/fonts/lato-v17-latin-regular.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: optional; /* Best for performance-critical text */
}

/* Preload critical fonts */
<link rel="preload" as="font" href="/fonts/lato-v17-latin-regular.woff2" type="font/woff2" crossorigin>

/* Use font-display: swap for body text */
@font-face {
  font-family: 'Lato';
  src: url('/fonts/lato-v17-latin-regular.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap; /* Good balance of performance and UX */
}
```

#### Reducing Font File Sizes
- **Subsetting**: Remove unused glyphs (especially for CJK fonts)
- **Compression**: Ensure WOFF2 is used (best compression)
- **Limit Variations**: Only load needed weights and styles
- **Use Variable Fonts**: Single file replaces multiple static fonts
- **Leverage Font Loading API**: Load fonts intelligently based on need

#### Critical Above-the-Fold Typography
```css
/* Inline critical font styles in HTML head */
<style>
  /* Critical above-the-fold styles */
  body { font-family: system-ui, sans-serif; }
  h1 { font-family: 'Inter', sans-serif; }
  
  /* Preload fonts */
  <link rel="preload" as="font" href="/fonts/inter-v12-latin-regular.woff2" type="font/woff2" crossorigin>
</style>

<!-- Deferred font loading -->
<link rel="stylesheet" href="/styles/main.css" media="print" onload="this.media='all'">
```

### 4. Responsive and Adaptive Typography
#### Fluid Typography with clamp()
```css
/* Fluid type that scales between minimum and maximum values */
h1 {
  font-size: clamp(2rem, 5vw, 4rem); /* Min: 2rem, Preferred: 5vw, Max: 4rem */
}

h2 {
  font-size: clamp(1.5rem, 4vw, 3rem);
}

p {
  font-size: clamp(1rem, 2.5vw, 1.25rem);
}

/* Viewport units with limits */
h1 {
  font-size: calc(1.5rem + 3vw); /* Base size plus viewport scaling */
  max-width: 80ch; /* Limit line length */
}
```

#### Modular Scaling with Breakpoints
```css
:root {
  /* Base scale */
  --font-size-base: 1rem;
  --ratio: 1.25;
}

/* Mobile-first approach */
h1 { font-size: calc(var(--font-size-base) * var(--ratio) * var(--ratio)); }
h2 { font-size: calc(var(--font-size-base) * var(--ratio)); }
p { font-size: var(--font-size-base); }

/* Tablet and up */
@media (min-width: 768px) {
  :root {
    --ratio: 1.333; /* Slightly larger ratio for bigger screens */
  }
  
  h1 { font-size: calc(var(--font-size-base) * var(--ratio) * var(--ratio) * var(--ratio)); }
  h2 { font-size: calc(var(--font-size-base) * var(--ratio) * var(--ratio)); }
  p { font-size: calc(var(--font-size-base) * var(--ratio)); }
}

/* Desktop and up */
@media (min-width: 1024px) {
  :root {
    --font-size-base: 1.125rem; /* Slightly larger base */
    --ratio: 1.5; /* More pronounced hierarchy */
  }
}
```

#### Direction-Aware Typography
```css
/* Handle both LTR and RTL layouts */
:root {
  --font-size-base: 1rem;
  --line-height: 1.5;
}

body {
  font-size: var(--font-size-base);
  line-height: var(--line-height);
  direction: ltr; /* Default, will be overridden by dir attribute */
}

/* Arabic-specific adjustments */
[dir="rtl"] body {
  /* May need different font family for better Arabic support */
  font-family: 'Noto Sans Arabic', 'Amiri', system-ui, sans-serif;
  
  /* Sometimes different spacing works better */
  line-height: 1.6;
}

/* Vertical writing modes (for Chinese, Japanese, Korean vertical text) */
.vertical-text {
  writing-mode: vertical-rl;
  /* May need different line height calculation */
  line-height: 1.4;
  text-orientation: mixed;
}
```

### 5. Accessibility Considerations
#### Scalable Typography
```css
/* Use relative units that respect user preferences */
:root {
  /* Base size - 16px browser default */
  --font-size-base: 1rem;
}

/* Ensure text scales properly */
html {
  font-size: 100%; /* Respect browser default */
}

/* Components should use rem or em */
.component {
  font-size: 1rem; /* 16px if browser default unchanged */
  padding: 1.5rem; /* Scales with font size */
}

/* Never override user base size in html/body */
html { 
  /* font-size: 62.5%; */ /* AVOID - breaks user preferences */
  /* 10px base is problematic for accessibility */
}

/* Maximum line length for readability */
@media (min-width: 480px) {
  .prose {
    max-width: 42ch; /* About 42 characters */
    margin-left: auto;
    margin-right: auto;
  }
}

/* Sufficient contrast */
.body-text {
  color: #222; /* Dark gray on white */
  background-color: #fff;
  /* 4.6:1 contrast ratio - meets WCAG AA */
}

.heading-text {
  color: #111; /* Even darker for headings */
  /* 7.1:1 contrast ratio - exceeds WCAG AA */
}

/* Avoid relying on color alone */
.error-message {
  color: #d32f2f; /* Red for error */
  border-left: 3px solid #d32f2f; /* Additional indicator */
  /* Icon with aria-label would be even better */
}
```

#### Respecting User Preferences
```css
/* Reduced motion preference */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.001ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.001ms !important;
  }
  
  /* Disable font animation effects */
  .font-effect {
    animation: none;
    transition: none;
  }
}

/* Increased contrast preference */
@media (prefers-contrast: more) {
  body {
    color: #000; /* Maximum contrast */
    background-color: #fff;
  }
  
  /* Enhance important UI elements */
  .button-primary {
    border-color: #000;
  }
}

/* Force colors preference */
@media (forced-colors: active) {
  /* Let system colors take over */
  button, a, input {
    /* Don't override forced colors */
  }
}
```

### 6. Advanced Techniques and Considerations

#### Optical Sizing
```css
/* Some fonts offer different designs for different sizes */
@font-face {
  font-family: 'Inter';
  src: url('/fonts/inter-display.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
  /* This is the display variant for large sizes */
}

@font-face {
  font-family: 'Inter';
  src: url('/fonts/inter-text.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
  /* This is the text variant for body sizes */
}

/* Usage with @supports */
@supports (font-variation-settings: normal) {
  /* Use variable font with optical size axis */
  :root {
    --font-body: 'Inter var';
    --font-display: 'Inter var';
  }
  
  body {
    font-family: var(--font-body);
    font-variation-settings: 'opsz' 16; /* Text size */
  }
  
  h1 {
    font-family: var(--font-display);
    font-variation-settings: 'opsz' 48; /* Display size */
  }
} /* Fallback to static fonts */
```

#### Color Fonts (SVGOT, COLR, CBDT)
```css
/* For fonts that support color (emoji, decorative fonts) */
@font-face {
  font-family: 'Twemoji Mozilla';
  src: url('/fonts/twemoji-color.woff2') format('woff2');
  /* Color font format */
}

/* Usage */
.emoji {
  font-family: 'Twemoji Mozilla', sans-serif;
}

/* Note: Browser support varies; always have fallback */
```

#### Variable Font Animation
```css
/* Animated variable font properties */
@keyframes font-weight-pulse {
  0%, 100% {
    font-variation-settings: 'wght' 400; /* Regular */
  }
  50% {
    font-variation-settings: 'wght' 700; /* Bold */
  }
}

.animated-heading {
  font-family: 'Inter var', sans-serif;
  font-variation-settings: 'wght' 400;
  animation: font-weight-pulse 3s ease-in-out infinite;
}

/* Hover effects */
.interactive-element {
  font-family: 'Inter var', sans-serif;
  transition: font-variation-settings 0.2s ease;
  
  font-variation-settings: 'wght' 400; /* Normal */
}

.interactive-element:hover {
  font-variation-settings: 'wght' 600; /* Semi-bold on hover */
}
```

#### Font Metrics and Fallback Compatibility
```css
/* Minimize layout shift with size-adjust */
@font-face {
  font-family: 'WebFont';
  src: url('/fonts/webfont.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
  /* Adjusts the font's aspect ratio to match fallback */
  /* Helps prevent layout shift when swapping */
  ascent-override: 90.5%;
  descent-override: 22.5%;
  line-gap-override: 0.0%;
}

/* Alternative: Use size-adjust shorthand (when supported) */
@font-face {
  font-family: 'WebFont';
  src: url('/fonts/webfont.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
  size-adjust: 105%; /* Adjust to match fallback metrics */
}

/* Matching x-height for better fallback compatibility */
@font-face {
  font-family: 'WebFont';
  src: url('/fonts/webfont.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
  
  /* Calculate based on fallback font */
  /* x-height ratio = webFont x-height / fallbackFont x-height */
  /* Example: if webFont x-height is 0.48em and fallback is 0.5em */
  /* size-adjust: 96%; */
}
```

## Testing and Validation Tools

### Performance Testing
- **Lighthouse**: Google's auditing tool includes font loading performance metrics
- **WebPageTest**: Advanced testing with filmstrip view to see font loading behavior
- **Chrome DevTools**: Network tab shows font loading; Performance tab shows rendering
- **Bundle Analyzers**: webpack-bundle-analyzer, rollup-plugin-visualize for font bundle analysis

### Rendering and Quality Testing
- **BrowserStack/Sauce Labs**: Cross-browser rendering testing
- **Font Drop**: Web-based font testing and comparison tool
- **Type Tester**: Side-by-side font comparison
- **WhatTheFont**: Font identification from images
- **wakamaifondue**: Background color and blending mode testing for fonts

### Accessibility Testing
- **WebAIM Contrast Checker**: Verifying color contrast ratios
- **axe DevTools**: Automated accessibility testing including text-related issues
- **Stark**: Contrast checking and color blindness simulation
- **Chrome Lighthouse**: Accessibility audit includes text scaling and contrast
- **Font Arbiter**: Comparing font rendering across platforms

### Internationalization Testing
- **Google's Noto Fonts**: Excellent for testing multilingual support
- **BabelPad**: Advanced Unicode text editor for testing complex scripts
- **Online RTL Demos**: Testing right-to-left language support
- **Localization Testing Frameworks**: i18next, FormatJS, etc. with linguistic testing

## Implementation Checklist

### [ ] Font Selection
- [ ] License verified for web use
- [ ] Character set includes needed languages/symbols
- [ ] File sizes optimized (WOFF2 preferred)
- [ ] Consider variable fonts for multiple weights/styles
- [ ] Test legibility at small sizes

### [ ] Performance Optimization
- [ ] Implement font-display strategy (swap for body, optional for non-critical)
- [ ] Preload critical above-the-fold fonts
- [ ] Subset fonts to remove unused glyphs
- [ ] Limit font variations to only what's needed
- [ ] Consider system font UI for interfaces

### [ ] CSS Implementation
- [ ] Use relative units (rem, em) for scalability
- [ ] Establish consistent typographic scale
- [ ] Define clear hierarchy with semantic class names
- [ ] Implement fallback font stacks
- [ ] Use @supports for feature detection when needed

### [ ] Accessibility Compliance
- [ ] Minimum 4.5:1 contrast ratio for body text (WCAG AA)
- [ ] Text resizable up to 200% without loss of content
- [ ] Avoid relying on color alone for information
- [ ] Respect user preferences (reduced motion, contrast, etc.)
- [ ] Ensure proper language attribution (lang attribute)

### [ ] Responsive Design
- [ ] Fluid typography using clamp() or viewport units with limits
- [ ] Appropriate line lengths (45-75 characters) across breakpoints
- [ ] Adjust hierarchy for different screen sizes
- [ ] Handle directionality (LTR/RTL) properly
- [ ] Consider vertical writing modes when needed

### [ ] Testing and Validation
- [ ] Test across target browsers and devices
- [ ] Verify performance with Lighthouse/WebPageTest
- [ ] Check accessibility with axe or similar tools
- [ ] Validate internationalization with target languages
- [ ] Test font loading behavior on slow connections

## Resources and Further Learning

### Essential Reading
- [Web Typography by Richard Rutter](https://www.amazon.com/Web-Typography-Designing-Typographic-Information/dp/0993283357)
- [Typography Handbook by Chris Palmer](https://github.com/chriscoyier/Typography-Handbook)
- [The Web Designer's Guide to Fonts by Jason CranfordTeague](https://www.amazon.com/Web-Designers-Guide-Fonts-CranfordTeague/dp/032181122X)
- [Designing with Web Fonts by Jason CranfordTeague & Stephen Boss](https://www.amazon.com/Designing-Web-Fonts-Jason-CranfordTeague/dp/1449309899)
- [Web Fonts Handbook by Bram Stein](https://webfonthandbook.com/)

### Online Resources and Tools
- [Google Fonts](https://fonts.google.com/) - Free, open-source fonts optimized for web
- [Fontsource](https://fontsource.org/) - Self-hostable open-source fonts
- [Adobe Fonts](https://fonts.adobe.com/) - Professional font library (subscription)
- [Font Squirrel](https://www.fontsquirrel.com/) - Free fonts with web kit generator
- [GitHub Font Collections**: Various open-source font collections
- [Variable Fonts](https://v-fonts.com/) - Resources and examples for variable fonts
- [Axis-Praxis](https://axis-praxis.org/) - Variable font experimentation tool
- [wakamaifondue](https://wakamaifondue.com/) - Background blend mode testing

### Specifications and Standards
- [WOFF 2.0 Specification](https://www.w3.org/TR/WOFF2/)
- [CSS Fonts Module Level 4](https://drafts.csswg.org/css-fonts-4/) (includes variable fonts)
- [CSS Font Loading Module Level 3](https://www.w3.org/TR/css-font-loading-3/)
- [OpenType Font Variations Overview](https://developer.apple.com/fonts/TrueType-Reference-Manual/RM06/Chap6.html)
- [W3C Internationalization Activity](https://www.w3.org/International/)

### Performance Guidelines
- [Google Web Fundamentals - Web Font Optimization](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/web-fonts)
- [MDN Web Docs - CSS Font Loading API](https://developer.mozilla.org/en-US/docs/Web/API/CSS_Font_Loading_API)
- [Web Vitals - CLS and Font Loading](https://web.dev/articles/cls#fonts)
- [CSS-Tricks - A Comprehensive Guide to Font Loading Strategies](https://css-tricks.com/font-loading-strategies/)

### Accessibility Resources
- [WCAG 2.1 Text Spacing](https://www.w3.org/TR/WCAG21/#text-spacing)
- [WebAIM - Typography and Accessibility](https://webaim.org/articles/visual/)
- [IBM Accessibility Checklist - Typography](https://www.ibm.com/able/guidelines/design/typography.html)
- [Material Design - Typography Accessibility](https://m3.material.io/styles/typography/accessibility)
- [Apple Accessibility - Typography](https://developer.apple.com/accessibility/)

### Testing Tools
- [Lighthouse](https://developers.google.com/web/tools/lighthouse)
- [WebPageTest](https://www.webpagetest.org/)
- [Font Drop](https://drop.typenetwork.com/)
- [Type Tester](https://www.typetester.org/)
- [Stark](https://getstark.co/)
- [axe DevTools](https://www.deque.com/axe/)
- [Accessibility Insights](https://accessibilityinsights.io/)