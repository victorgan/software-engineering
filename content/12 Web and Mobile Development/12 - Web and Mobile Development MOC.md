# 12 — Web and Mobile Development MOC

> <- Back to [[Software Engineering - Map of Content]]

Building user-facing applications for browsers and mobile devices. The most visible layer of software — where users actually interact with what we build.

---

## Web Fundamentals

- **HTML Semantics** — Semantic elements (header, nav, main, article, section, aside, footer), accessibility implications, SEO benefits
- **CSS Box Model** — Content, padding, border, margin; box-sizing: border-box vs content-box
- **CSS Layout** — Flexbox (main axis, cross axis, flex-grow/shrink/basis), Grid (tracks, areas, fr units, auto-fit/auto-fill), float (legacy)
- **CSS Specificity** — Inline > ID > class > element, specificity calculation, !important escape hatch, cascade layers (@layer)
- **DOM (Document Object Model)** — Tree structure, nodes, event delegation, event bubbling/capturing, DOM manipulation APIs
- **Browser Rendering Pipeline** — Parse HTML → build DOM, parse CSS → build CSSOM, combine → Render Tree → Layout → Paint → Composite
- **Critical Rendering Path** — Render-blocking resources, async/defer scripts, CSS optimization, minimizing critical resources
- **CSSOM** — CSS Object Model, style computation, recalculation costs

---

## JavaScript & the Browser

- **Event Loop** — Call stack, task queue (macrotasks), microtask queue, requestAnimationFrame, event loop phases
- **Call Stack** — Execution contexts, stack overflow, single-threaded execution
- **Microtasks vs Macrotasks** — Microtasks (Promise.then, queueMicrotask, MutationObserver) run before macrotasks (setTimeout, setInterval, I/O)
- **Web APIs** — fetch, localStorage, sessionStorage, IndexedDB, Web Workers, Service Workers, Geolocation, Notification API
- **Web Workers** — Background threads, postMessage, SharedArrayBuffer, Comlink
- **Service Workers** — Proxy between browser and network, offline support, push notifications, cache strategies (see Browser APIs & PWAs below)
- **Module Systems** — ESM (import/export, tree-shakeable, async), CommonJS (require/module.exports, synchronous, Node.js), UMD, IIFE (legacy)

---

## Frontend Frameworks

- **React** — Hooks (useState, useEffect, useMemo, useCallback, useRef, custom hooks), virtual DOM, reconciliation (diffing algorithm), React Server Components (RSC), Suspense, concurrent features
- **Vue** — Composition API, reactivity system (Proxy-based), single-file components, Nuxt (meta-framework)
- **Angular** — Dependency injection, RxJS, signals, zones, standalone components, NgModules (legacy)
- **Svelte** — Compile-time framework, no virtual DOM, reactive assignments, SvelteKit (meta-framework)
- **Signals & Reactivity Patterns** — Fine-grained reactivity (Solid, Preact Signals, Angular Signals, Vue refs), push vs pull, dependency tracking
- **State Management** — Redux (actions, reducers, middleware, Redux Toolkit), Zustand (minimal, hooks-based), Pinia (Vue), Jotai/Recoil (atomic), XState (state machines)
- **Rendering Strategies** — SSR (Server-Side Rendering), CSR (Client-Side Rendering), SSG (Static Site Generation), ISR (Incremental Static Regeneration), streaming SSR, partial hydration, islands architecture

---

## Web Performance

- **Core Web Vitals** — LCP (Largest Contentful Paint), FID/INP (First Input Delay / Interaction to Next Paint), CLS (Cumulative Layout Shift)
- **Lighthouse** — Performance audits, scoring, lab vs field data, PageSpeed Insights
- **Bundle Size** — Analyzing bundles (webpack-bundle-analyzer, source-map-explorer), reducing dependencies, dynamic imports
- **Code Splitting** — Route-based splitting, component-level splitting, dynamic import(), React.lazy
- **Lazy Loading** — Images (loading="lazy", Intersection Observer), components, routes, below-the-fold content
- **Image Optimization** — Modern formats (WebP, AVIF), responsive images (srcset, sizes), picture element, CDN-based transforms
- **Tree Shaking** — Dead code elimination, ESM requirement, side effects (sideEffects field in package.json)
- **Resource Hints** — prefetch (future navigations), preload (current page critical resources), preconnect, dns-prefetch, modulepreload

---

## Build Tooling

- **Bundlers** — Webpack (loaders, plugins, code splitting, HMR), Vite (ESM dev server, Rollup-based production), esbuild (Go-based, extremely fast), Turbopack (Rust-based, Webpack successor), Rollup (library-focused)
- **Transpilers** — Babel (JSX, TC39 proposals, polyfills), SWC (Rust-based Babel alternative, used by Next.js/Vite), TypeScript compiler (tsc)
- **CSS Processing** — PostCSS (plugins, autoprefixer, cssnano), Tailwind CSS (utility-first, JIT), CSS Modules, CSS-in-JS (styled-components, Emotion), Sass/Less (legacy)
- **Monorepo Tools** — Nx (computation caching, affected commands, generators), Turborepo (pipeline-based caching, Vercel), pnpm workspaces, Lerna (legacy)
- **Task Runners & Scripts** — npm scripts, Makefiles, Just, package.json scripts composition

---

## Accessibility (a11y)

- **WCAG Guidelines** — Web Content Accessibility Guidelines, levels A/AA/AAA, POUR principles (Perceivable, Operable, Understandable, Robust)
- **ARIA Roles** — Landmarks, widgets, live regions, aria-label, aria-describedby, aria-hidden, aria-expanded
- **Semantic HTML** — Using correct elements (button vs div, nav, heading hierarchy), implicit roles, reducing ARIA need
- **Screen Readers** — VoiceOver (macOS/iOS), NVDA (Windows), JAWS, TalkBack (Android), how they navigate the accessibility tree
- **Keyboard Navigation** — Tab order, focus management, skip links, roving tabindex, keyboard traps
- **Color Contrast** — WCAG contrast ratios (4.5:1 normal text, 3:1 large text), tools (axe, Colour Contrast Analyser)
- **Focus Management** — Focus trapping in modals, restoring focus, focus-visible, outline styles

---

## Browser APIs & PWAs

- **Service Workers** — Lifecycle (install, activate, fetch), cache strategies (cache-first, network-first, stale-while-revalidate), background sync
- **Cache API** — Programmatic cache management, cache versioning, cache cleanup
- **Web Push** — Push API, Notification API, VAPID keys, push subscription management
- **Web App Manifest** — manifest.json, icons, display modes (standalone, fullscreen), theme color, start URL
- **Offline-First** — Offline detection (navigator.onLine), queuing actions, conflict resolution, IndexedDB for offline storage
- **WebSockets vs SSE** — WebSockets (full-duplex, binary support), Server-Sent Events (one-way, auto-reconnect, simpler), choosing between them (see [[Networking]])
- **WebRTC** — Peer-to-peer communication, signaling, STUN/TURN servers, media streams, data channels

---

## Frontend Testing

- **Component Testing** — Testing Library (React, Vue, Angular), render + query + assert, user-event, testing behavior not implementation
- **Visual Regression Testing** — Chromatic (Storybook-based), Percy (BrowserStack), screenshot comparison, pixel diffing
- **End-to-End Testing** — Playwright (multi-browser, auto-wait, codegen), Cypress (developer experience, time-travel debugging), test isolation, flaky test management
- **Storybook** — Component development in isolation, stories, addons (a11y, interactions, viewport), visual testing integration, design system documentation
- **Unit Testing** — Jest, Vitest, testing utility functions and hooks, mocking modules
- **Performance Testing** — Lighthouse CI, Web Vitals measurement, bundle size checks in CI

---

## Mobile Development

- **iOS** — Swift (protocol-oriented, value types, optionals), UIKit (imperative, Auto Layout), SwiftUI (declarative, state management, previews), Xcode, Combine (reactive framework)
- **Android** — Kotlin (null safety, coroutines, data classes), Jetpack Compose (declarative UI), Jetpack libraries (ViewModel, Room, Navigation), Android Studio, Gradle
- **Cross-Platform** — React Native (JavaScript, native bridge, Hermes engine, New Architecture with Fabric/TurboModules), Flutter (Dart, widget tree, Skia rendering, hot reload), Kotlin Multiplatform (shared business logic, native UI)
- **Mobile Lifecycle** — App states (foreground, background, suspended), state restoration, memory warnings, background execution limits
- **Push Notifications** — APNs (Apple), FCM (Firebase Cloud Messaging), notification channels, silent notifications, rich notifications
- **Deep Linking** — URL schemes, Universal Links (iOS), App Links (Android), deferred deep linking, deep link routing
- **Offline Storage** — SQLite, Core Data (iOS), Room (Android), Realm, encrypted storage, sync strategies
- **App Distribution** — App Store (review process, TestFlight, guidelines), Play Store (review, internal testing tracks), enterprise distribution, OTA updates (CodePush, Expo Updates)

---

## Internationalization & Localization (i18n/l10n)

- **Unicode & UTF-8** — Character encoding, code points, grapheme clusters, surrogate pairs, normalization forms (NFC, NFD)
- **ICU Message Format** — Standard syntax for plurals, select, and nested messages; used by FormatJS, ICU4J
- **Locale-Aware Formatting** — Dates (Intl.DateTimeFormat), numbers (Intl.NumberFormat), currency, relative time, list formatting
- **Pluralization Rules** — CLDR plural categories (zero, one, two, few, many, other), language-specific rules
- **RTL Layouts** — Logical properties (inline-start/end vs left/right), CSS direction, writing modes, bidirectional text (bidi algorithm)
- **Translation Workflows** — String extraction, translation management systems (Crowdin, Lokalise, Phrase), pseudo-localization, context for translators
- **i18n Libraries** — react-intl / FormatJS, i18next (framework-agnostic), vue-i18n, angular/localize, ICU4J (Java)
- **Time Zones** — IANA tz database (e.g., America/New_York), UTC as storage format, daylight saving transitions, Temporal API (TC39 proposal), Luxon/date-fns-tz

---

#web #frontend #mobile #accessibility #performance #pwa #i18n
