# Frontend File Map

Complete breakdown of every file in `frontend/` and what it does.

---

## `src/` (source code)

### Entry Points

| File | Role |
| --- | --- |
| `src/index.js` | Mounts `App` into the DOM via `createRoot` with StrictMode. |
| `src/App.js` | Root component: wraps everything in `AuthProvider` + `BrowserRouter` + `ToastContainer` (top-right, dark theme). Defines routes: `/` (LandingPage), `/login` (LoginPage), `/signup` (SignupPage), `/terminal` (TradingTerminal behind PrivateRoute). |

### Pages (`src/pages/`)

| File | Role |
| --- | --- |
| `LandingPage.js` | FundedHive-styled landing page: hero section with stats, video demo section (`crypto_terminal_demo.mp4` autoplay/loop/muted), features grid (6 cards with images), 3-step how-it-works (gold numbered circles + arrow SVGs), FAQ accordion (6 items, single open at a time), CTA section, footer. Nav bar with gold links, hamburger menu on mobile (<768px) with centered dropdown. Smooth scrolling via `scroll-behavior: smooth` + `scroll-padding-top: 80px`. |
| `LoginPage.js` | Login form (email + password). Calls `login()` from AuthContext, redirects to `/terminal` on success. Shows error on failure. Toast notification on success. |
| `SignupPage.js` | Signup form (name + email + password). Calls `register()` from AuthContext, redirects to `/terminal` on success. Validates password >= 6 chars. Toast notification on success. |

### Components (`src/components/`)

| File | Role |
| --- | --- |
| `CandlestickChart.js` | Orchestrates the chart: chart setup, drawing tools, overlay lines, indicators, crosshair tooltip, measure popup, trendline popup, fullscreen toggle. |
| `ChartOverlay.js` | Shows a loading spinner or error message over the chart while data loads. |
| `ChartSettings.js` | "Vol" toggle button and fullscreen button. |
| `ChartTooltip.js` | Floating OHLCV tooltip that follows the crosshair. |
| `ChartTypeSelector.js` | Button group to switch Candlestick / Line / Area / Bar chart types. |
| `DrawingToolbar.js` | SVG icon buttons for trend line, horizontal line, measure tool, and clear-all. |
| `IndicatorSelector.js` | Toggle buttons for SMA, EMA, RSI, Bollinger Bands + clear button. |
| `MeasurePopup.js` | Floating popup showing ΔPrice, Δ%, and time span between two measured points. Supports live data mode. |
| `PrivateRoute.js` | Auth guard: shows loading state while checking auth, redirects to `/login` if no user, renders children if authenticated. |
| `SmallScreenNotice.js` | Full-screen overlay telling phone users (<768px) to use a laptop/tablet. |
| `TradingTerminal.js` | Core terminal: coin sidebar, chart, order form, positions/orders/history tabs, live WebSocket tickers, auto SL/TP/limit triggers, portfolio display, user profile dropdown (avatar + name + ChevronDown), demo reset, logout. All API calls include Bearer token via `authHeaders` (useMemo for stable reference). Toast notifications on trade events. |
| `TrendlinePopup.js` | Floating popup to edit a trend line's color, line style (solid/dashed/dotted), and delete it. Position clamped within chart bounds. Closes on tool select, clear-all, or clicking empty chart area. |

### Context (`src/context/`)

| File | Role |
| --- | --- |
| `AuthContext.js` | Auth state management: provides `user`, `token`, `loading`, `login()`, `register()`, `logout()`. Auto-loads token from localStorage and fetches `/api/auth/me` on mount. |

### Hooks (`src/hooks/`)

| File | Role |
| --- | --- |
| `useChartSetup.js` | Creates/manages the Lightweight Charts instance: fetches klines from Binance REST API, opens real-time kline WebSocket, handles chart type changes, volume bar series, window resize. |
| `useDrawingTools.js` | Interactive drawing tools: click-to-place trend/horizontal/measure lines, tracking line while placing, hover detection (pointer cursor), trendline persistence across chart recreation via `pendingRestoreRef`, style editing, `triggeringInFlight` ref to prevent duplicate API calls. |
| `useIndicators.js` | Computes and renders SMA (7/25/99), EMA (12/26), RSI (14 with OB/OS lines at 70/30), Bollinger Bands (20/2) as overlay series on the chart. |
| `useOverlayLines.js` | Draws dashed price lines for SL/TP and dotted lines for pending limit orders on the chart. Uses `recentlyUpdatedSLTP` Set to suppress auto-trigger after manual save. |

### Utilities (`src/utils/`)

| File | Role |
| --- | --- |
| `binanceData.js` | `fetchKlines()` (REST call for historical candles) and `createKlineSocket()` (WebSocket for real-time kline updates). |
| `chartConfig.js` | Chart layout/theme options, series configs (Candle/Line/Area/Bar), volume options, `createChartOptions()`, `formatKline()` / `formatLiveCandle()`. |
| `chartHelpers.js` | `distanceToSegment()` (Euclidean distance to line segment — used for trendline hover detection) and `getBinanceSymbol()` (coin → "BTCUSDT"). |
| `indicators.js` | Pure functions: SMA, EMA, RSI, Bollinger Bands calculations. |

### Styles (`src/styles/`)

| File | Role |
| --- | --- |
| `App.css` | Complete dark-theme stylesheet: `:root` CSS variables (`--lh-gold`, `--lh-black`, `--lh-card`, etc.), terminal layout (header/sidebar/chart/panel), tables, drawing toolbar, form inputs, alerts, animations, scrollbar, responsive notice, trendline popup. FundedHive landing page + auth page styles (Space Grotesk / Onest fonts, gold-on-black theme, hexagonal background). Hamburger menu with centered dropdown on mobile. FAQ accordion styles. Profile dropdown styles. Responsive breakpoints. |
| `index.css` | Global body reset (removes default margin). |

---

## `public/` (static assets)

| File | Role |
| --- | --- |
| `index.html` | HTML entry with SEO meta tags, OG/Twitter cards, JSON-LD structured data, favicon links, font preloads. |
| `manifest.json` | PWA manifest: app name, description, icons, display mode, theme/background colors. |
| `site.webmanifest` | Alternate minimal PWA manifest. |
| `robots.txt` | Allows all crawlers (including GPTBot, Claude-Web, PerplexityBot); sets `ai-train=no`, `search=yes`, `ai-input=no`. |
| `sitemap.xml` | XML sitemap with root URL and daily change frequency. |
| `_headers` | Netlify custom headers with RFC 8288 Link headers for agent discovery (service-doc, sitemap, API catalog). |
| `favicon.ico` | Legacy multi-size favicon. |
| `favicon-16x16.png` | 16x16 favicon PNG. |
| `favicon-32x32.png` | 32x32 favicon PNG. |
| `apple-touch-icon.png` | iOS home-screen icon (180x180). |
| `android-chrome-192x192.png` / `android-chrome-512x512.png` | PWA icons. |
| `crypto_terminal_demo.mp4` | Demo video for landing page (autoplay, loop, muted). |
| `candle_chart.png` | Feature card image — candlestick chart. |
| `area_chart.png` | Feature card image — area chart. |
| `indicators.png` | Feature card image — technical indicators. |
| `trendline.png` | Feature card image — trendline drawing. |
| `measurement.png` | Feature card image — measurement tool. |
| `open_position.png` | Feature card image — open positions. |
| `trade_history.png` | Feature card image — trade history. |

---

## `netlify/` (edge infrastructure)

| File | Role |
| --- | --- |
| `netlify.toml` | Build config: publish dir `build`, edge functions dir `netlify/edge-functions`, edge function on `/`. |
| `netlify/edge-functions/markdown-negotiation.js` | Edge Function that returns a Markdown description when `Accept: text/markdown` is sent, enabling AI-agent consumption. |

---

## `analysis/` (documentation)

| File | Role |
| --- | --- |
| `uiDesign.md` | FundedHive-inspired design system: color palette, typography, component styles, layout principles, responsive behavior, agent prompt guide. |
| `projectStructure.md` | This file — complete file-by-file breakdown of the frontend. |
