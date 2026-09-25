ATAS Account Info & Custom Risk HUD (Account Info Custom)
A feature-rich, high-performance C# custom indicator for ATAS (Advanced Trade Analysis System) designed to give futures traders a clean on-screen HUD. It tracks live account balances, manages risk parameters (Daily Loss Limits & Trailing Drawdowns), provides audio alerts, and overlays past execution metrics and real-time PnL visualizers directly onto your charts.

✨ Key Features
Account HUD: Real-time tracking of Account ID (with built-in obfuscation), Currency, Balance, Available Balance, Blocked Margin, Leverage, and Open/Closed/Total PnL.

Global Active Position Monitor: Automatically detects if a trade is running on the active account and pops up an [ACTIVE TRADE] warning banner to prevent leaving positions open in background windows.

Visual PnL Risk Slider: A dynamic status bar at the bottom of the HUD that visualizes your current distance to your Daily Loss Limit or profit target. Supports open-ended mode (where the 0 marker shifts to the right edge to maximize loss-limit visualization).

Trailing Drawdown & Buffer Tracking: Automatically logs high-water marks and monitors your safety buffer against Daily Loss Limits and trailing drawdowns in real-time.

Trade History & Custom Markers: Renders past trades directly on the chart with customizable entry triangles, connecting execution lines, and interactive tooltips.

Today’s Statistics Grid: Calculates and displays daily performance analytics (Total Trades, Win Rate, Edge / Performance Ratio, Expectancy/EV, Profit Factor, Best/Worst trades, and Avg Win/Loss) split cleanly into a 2-column format.

Priority Audio Alerts: Built-in sound triggers for position entries, trade wins/losses, profit target hits, and daily loss limit warnings.

Commission Management: Option to dynamically pull native feed commissions or apply a manual per-contract commission override.

🛠️ Installation & Setup
Prerequisites: Make sure you have ATAS installed and a working development environment (Visual Studio with .NET support) if compiling from source.

Add to ATAS:

Place the .cs file inside your ATAS custom indicators directory (typically located at %APPDATA%\ATAS\Indicators).

Alternatively, open your ATAS platform, open the indicator editor, create a new indicator, paste the source code, and click Compile.

Attach to Chart: Open any chart in ATAS, press Ctrl + I, navigate to the Custom category, and select Account Info(Custom).

⚙️ Configuration Parameters
You can customize the indicator entirely from the ATAS properties panel:

Visualization: Adjust background colors, text colors, positive/negative PnL accent colors, and font sizing.

Risk Management: Set your Profit Target ($), Daily Loss Limit ($), enable Trailing Drawdown, and toggle the visual PnL slider. (Note: Setting the Profit Target to 0 automatically shifts the slider into an open-ended risk mode, dedicating 100% of the bar width to visualizing your drawdown buffer).

Trade Visualization: Toggle trade lines, tooltips, marker sizes, label display modes (Hide, Short, Full), and custom Buy/Sell line dash styles and colors.

Stats Configuration: Choose which individual daily metrics (Edge, EV, Win Rate, Profit Factor, etc.) you want displayed in the HUD stats grid.

Audio Alerts: Bind custom sound effects to execution events and risk threshold breaches.

Commission Settings: Toggle commission deductions and set manual overrides per contract.

🧩 Requirements
ATAS Platform (Version 8.x or higher featuring custom indicator support).

Compatible data feed supporting trading metrics and historical trade statistics (e.g., Rithmic, CQG).

📄 License
This project is open-source and free for personal and community use. Feel free to modify and adapt it to your trading workflow!
