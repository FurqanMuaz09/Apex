# APEX Exchange — Android source prototype

This project packages the APEX mobile-first web interface in an Android WebView.

## Included in this iteration
- Binance public 24-hour ticker API refresh (15-second polling)
- Public kline chart API with 1m, 15m, 1h, 4h, and 1d intervals
- Select a market row to switch the trading pair
- Search and gainers/losers market filters
- Market/Limit/Stop-limit selector UI and estimated total calculation
- No fabricated account balance; private account screens remain explicitly disconnected
- Android WebView asset loader and Internet permission

## Build Android APK
1. Open this `apex-android` folder in Android Studio on a computer with Android SDK 35 installed.
2. Allow Gradle sync.
3. Select **Build > Build APK(s)** for a test APK, or **Build > Generate Signed Bundle / APK** for a release build.

This runtime does not contain Android SDK/Gradle build tools, so an APK binary could not be compiled or tested here. The included files are Android source, not an installable APK.

## Binance connection boundary
Only public market data is implemented. There is no Binance account login, private balance endpoint, real order placement, deposits, or withdrawals. Do not place API keys or secrets in the app. A next phase should add a server-side integration tested against Binance Spot Testnet, with API-key permission restrictions, authentication, request signing on the server, rate limits, order validation, audit logs, and explicit risk controls. Withdrawals should remain disabled.
