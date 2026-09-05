# Open (https://eriol-0406.github.io/btc-loan-calculator/) to preview

📊 BTC Borrowing Power Calculator (MYR)

A sleek, browser-based Bitcoin loan calculator that fetches live BTC/MYR prices, applies tenure-based interest rates, and displays a 7-day price trend chart — no backend required.


✨ Features

Live BTC/MYR Chart — chart.html shows a TradingView-style candlestick chart (1m to 1H timeframes) that refreshes once per minute from Binance public market data, converted to MYR with a reference USD/MYR rate.
Live BTC/MYR Price — Automatically fetches the current Bitcoin price in Malaysian Ringgit via the CoinGecko API on load.
Collateral-Based Borrowing — Calculates your maximum borrow amount using a 70% Loan-to-Value Ratio (LVR) against your BTC holdings.
Tenure-Based Interest Rates — Interest rate adjusts automatically based on your chosen loan tenure:
Tenure Annual Interest Rate
3 – 12 months  12.0%
13 – 24 months 11.5%
25 – 36 months 11.0%
37 – 48 months 10.5%
49 – 60 months 10.0%

Interactive Tenure Slider — Drag the slider (3–60 months) or use quick-select tier buttons to choose your loan period.
Full Cost Breakdown — Displays borrow amount, 0.5% stamp fee, total interest payable, and total repayment amount.
Quarterly Payment Schedule — Auto-generates upcoming quarterly interest payment dates based on your selected tenure.
7-Day Price Trend Chart — Renders a live sparkline chart of BTC/MYR price over the past 7 days.
Offline Fallback — Gracefully falls back to a preset BTC price if the API is unreachable.


🚀 Getting Started
No installation or build step needed. This is a single HTML file.

Download or clone this repository.
Open btc_loan_calc.html in any modern web browser (Chrome, Firefox, Edge, Safari).
That's it — the calculator will load and fetch the live BTC price automatically.

🧮 How It Works
The calculator uses the following formulas:
Borrow Amount   = BTC Amount × BTC Price × 0.70 (LVR)
Stamp Fee       = Borrow Amount × 0.005 (0.5%)
Interest        = Borrow Amount × Annual Rate × (Months / 12)
Total Payable   = Borrow Amount + Stamp Fee + Interest
Interest rates are tiered by tenure — the longer your loan, the lower your annual rate.

🔌 API Used
ProviderEndpointPurposeCoinGecko/simple/priceLive BTC/MYR spot priceCoinGecko/coins/bitcoin/market_chart7-day historical price data

The free CoinGecko API is used without an API key. Rate limits may apply for frequent use.


📦 Dependencies
All dependencies are loaded via CDN — no npm install required.
LibraryVersionPurposeChart.jsLatestTrend line chartchartjs-plugin-datalabelsv2Price labels on chartGoogle Fonts (Space Mono, DM Sans)—Typography

⚠️ Disclaimer
This calculator is for informational and illustrative purposes only. It does not constitute financial advice. Actual loan terms, interest rates, fees, and LVR may vary depending on your lender. Bitcoin is a highly volatile asset — past price appreciation does not guarantee future returns.

📈 Note: Bitcoin has historically appreciated approximately ~8% annually on a long-term average basis. (Source: Macrotrends)


📄 License
MIT License. Free to use, modify, and distribute.


📊 BTC 借款计算器（马来西亚令吉）

一款简洁的浏览器端比特币贷款计算器，可实时获取 BTC/MYR 价格、根据贷款期限自动调整利率，并展示 7 天价格走势图——无需后端服务。


✨ 功能特点

实时 BTC/MYR 价格 — 页面加载时通过 CoinGecko API 自动获取比特币最新马来西亚令吉报价。
抵押品借款计算 — 以您的 BTC 持仓为抵押，按 70% 贷款价值比（LVR）计算最高可借金额。
分期利率体系 — 利率根据您选择的贷款期限自动调整：
贷款期限年利率
3 – 12  个月 12.0%
13 – 24 个月 11.5%
25 – 36 个月 11.0%
37 – 48 个月 10.5%
49 – 60 个月 10.0%

交互式期限滑块 — 拖动滑块（3–60 个月）或点击快捷选择按钮，灵活设定贷款期限。
费用全面拆解 — 显示借款金额、0.5% 印花税、总利息及总还款金额。
季度还款计划 — 根据所选期限自动生成未来各期季度利息还款日期。
7 天价格走势图 — 以折线图形式展示过去 7 天 BTC/MYR 实时价格走势。
离线降级处理 — API 无法访问时，自动使用预设 BTC 价格，确保计算器正常使用。


🚀 快速开始
无需安装或构建，本项目为单一 HTML 文件。

下载或克隆本仓库。
使用任意现代浏览器（Chrome、Firefox、Edge、Safari）直接打开 btc_loan_calc.html。
完成！计算器会自动加载并获取实时 BTC 价格。

🧮 计算逻辑
计算器使用以下公式：
可借金额   = BTC 数量 × BTC 价格 × 0.70（LVR）
印花税     = 可借金额 × 0.005（0.5%）
总利息     = 可借金额 × 年利率 × （月数 / 12）
总还款额   = 可借金额 + 印花税 + 总利息
利率按期限分档——贷款期越长，年利率越低。

🔌 使用的 API
数据来源接口端点用途CoinGecko/simple/price实时 BTC/MYR 现货价格CoinGecko/coins/bitcoin/market_chart7 天历史价格数据

本项目使用 CoinGecko 免费公共 API，无需 API Key。频繁请求可能受到速率限制。


📦 依赖项
所有依赖均通过 CDN 加载，无需执行 npm install。
库名称版本用途Chart.js最新版趋势折线图chartjs-plugin-datalabelsv2图表价格标签Google Fonts（Space Mono、DM Sans）—字体排版

⚠️ 免责声明
本计算器仅供参考和演示用途，不构成任何财务建议。实际贷款条款、利率、费用及贷款价值比（LVR）可能因贷款机构而有所不同。比特币属于高波动性资产，历史价格走势不代表未来收益。

📈 注意：比特币历史上长期年均升值约 ~8%，但这不保证未来表现。（数据来源：Macrotrends）


📄 开源许可
MIT 许可证。可自由使用、修改与分发。
