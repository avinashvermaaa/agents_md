# Frontend File Map

Complete breakdown of every file in `frontend/` and what it does.

---

## `src/` (source code)

### Entry Points

| File | Role |
|---|---|
| `src/index.js` | Mounts `App` into the DOM via `createRoot` with StrictMode. |
| `src/App.js` | Root component: wraps everything in `AuthProvider` + `BrowserRouter`. Defines routes: `/` (LandingPage), `/login` (LoginPage), `/signup` (SignupPage), `/terminal` (TradingTerminal behind PrivateRoute). |

### Pages (`src/pages/`)

| File | Role |
|---|---|
| `LandingPage.js` | FundedHive-styled landing page: hero section, features grid (6 cards), 3-step how-it-works, CTA section, footer. Gold-on-black premium theme with hexagonal background pattern. |
| `LoginPage.js` | Login form (email + password). Calls `login()` from AuthContext, redirects to `/terminal` on success. Shows error on failure. |
| `SignupPage.js` | Signup form (name + email + password). Calls `register()` from AuthContext, redirects to `/terminal` on success. Validates password >= 6 chars. |

### Components (`src/components/`)

| File | Role |
|---|---|
| `CandlestickChart.js` | Orchestrates the chart: chart setup, drawing tools, overlay lines, indicators, crosshair tooltip, measure popup, trendline popup, fullscreen toggle. |
| `ChartOverlay.js` | Shows a loading spinner or error message over the chart while data loads. |
| `ChartSettings.js` | "Vol" toggle button and fullscreen button. |
| `ChartTooltip.js` | Floating OHLCV tooltip that follows the crosshair. |
| `ChartTypeSelector.js` | Button group to switch Candlestick / Line / Area / Bar chart types. |
| `DrawingToolbar.js` | SVG icon buttons for trend line, horizontal line, measure tool, and clear-all. |
| `IndicatorSelector.js` | Toggle buttons for SMA, EMA, RSI, Bollinger Bands + clear button. |
| `MeasurePopup.js` | Floating popup showing ΔPrice, Δ%, and time span between two measured points. |
| `PrivateRoute.js` | Auth guard: shows loading state while checking auth, redirects to `/login` if no user, renders children if authenticated. |
| `SmallScreenNotice.js` | Full-screen overlay telling phone users to use a laptop/tablet. |
| `TradingTerminal.js` | Core terminal: coin sidebar, chart, order form, positions/orders/history tabs, live WebSocket tickers, auto SL/TP/limit triggers, portfolio display, demo reset, logout button. All API calls include Bearer token via `authHeaders`. |
| `TrendlinePopup.js` | Floating popup to edit a trend line's color, line style (solid/dashed/dotted), and delete it. |

### Context (`src/context/`)

| File | Role |
|---|---|
| `AuthContext.js` | Auth state management: provides `user`, `token`, `loading`, `login()`, `register()`, `logout()`. Auto-loads token from localStorage and fetches `/api/auth/me` on mount. |

### Hooks (`src/hooks/`)

| File | Role |
|---|---|
| `useChartSetup.js` | Creates/manages the Lightweight Charts instance: fetches klines from Binance REST API, opens real-time kline WebSocket, handles chart type changes, volume bar series, window resize. |
| `useDrawingTools.js` | Interactive drawing tools: click-to-place trend/horizontal/measure lines, tracking line while placing, hover detection (pointer cursor), trendline persistence across chart recreation, style editing. |
| `useIndicators.js` | Computes and renders SMA, EMA, RSI (with OB/OS lines), Bollinger Bands as overlay series on the chart. |
| `useOverlayLines.js` | Draws dashed price lines for SL/TP and dotted lines for pending limit orders on the chart. |

### Utilities (`src/utils/`)

| File | Role |
|---|---|
| `binanceData.js` | `fetchKlines()` (REST call for historical candles) and `createKlineSocket()` (WebSocket for real-time kline updates). |
| `chartConfig.js` | Chart layout/theme options, series configs (Candle/Line/Area/Bar), volume options, `createChartOptions()`, `formatKline()` / `formatLiveCandle()`. |
| `chartHelpers.js` | `distanceToSegment()` (Euclidean distance to line segment — used for trendline hover detection) and `getBinanceSymbol()` (coin → "BTCUSDT"). |
| `indicators.js` | Pure functions: SMA, EMA, RSI, Bollinger Bands calculations. |

### Styles (`src/styles/`)

| File | Role |
|---|---|
| `App.css` | Complete dark-theme stylesheet: CSS custom properties, terminal layout (header/sidebar/chart/panel), tables, drawing toolbar, form inputs, alerts, animations, scrollbar, responsive notice, trendline popup. Includes FundedHive landing page + auth page styles (Space Grotesk / Onest fonts, gold-on-black theme, hexagonal background, responsive breakpoints). |
| `index.css` | Global body reset (removes default margin). |

---

## `public/` (static assets)

| File | Role |
|---|---|
| `index.html` | HTML entry with SEO meta tags, OG/Twitter cards, JSON-LD structured data, favicon links, font preloads. |
| `manifest.json` | PWA manifest: app name, description, icons, display mode, theme/background colors. |
| `site.webmanifest` | Alternate minimal PWA manifest. |
| `robots.txt` | Allows all crawlers (including GPTBot, Claude-Web, PerplexityBot); sets `ai-train=no`, `search=yes`, `ai-input=no`. |
| `sitemap.xml` | XML sitemap with root URL and daily change frequency. |
| `_headers` | Netlify custom headers with RFC 8288 Link headers for agent discovery (service-doc, sitemap, API catalog). |
| `favicon.ico` | Legacy multi-size favicon. |
| `favicon-16x16.png` | 16×16 favicon PNG. |
| `favicon-32x32.png` | 32×32 favicon PNG. |
| `apple-touch-icon.png` | iOS home-screen icon (180×180). |
| `android-chrome-192x192.png` / `android-chrome-512x512.png` | PWA icons. |

---

## `netlify/` (edge infrastructure)

| File | Role |
|---|---|
| `netlify.toml` | Build config: publish dir `build`, edge functions dir `netlify/edge-functions`, edge function on `/`. |
| `netlify/edge-functions/markdown-negotiation.js` | Edge Function that returns a Markdown description when `Accept: text/markdown` is sent, enabling AI-agent consumption. |

---

## `analysis/` (documentation)

| File | Role |
|---|---|
| `uiDesign.md` | FundedHive-inspired design system: color palette, typography, component styles, layout principles, responsive behavior, agent prompt guide. |
| `projectStructure.md` | This file — complete file-by-file breakdown of the frontend. |
