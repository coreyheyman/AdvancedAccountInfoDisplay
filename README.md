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

Take a look:

<img width="489" height="466" alt="Screenshot 2026-09-25 131318" src="https://github.com/user-attachments/assets/fab27ed9-d01b-46bd-8ad3-702921c15d62" />
<img width="608" height="864" alt="Screenshot 2026-09-25 131639" src="https://github.com/user-attachments/assets/b5e000ef-8a23-4dfe-9a4f-307ae0f7bd40" />
<img width="609" height="860" alt="Screenshot 2026-09-25 131656" src="https://github.com/user-attachments/assets/1e01bdf2-52b4-49ec-ad59-a83f6f8905ed" />
<img width="612" height="859" alt="Screenshot 2026-09-25 131712" src="https://github.com/user-attachments/assets/744b5dac-2182-4dcf-899c-cf55ad74e5da" />

Instructions:

Option A: Installing via Compiled .dll File (Easiest)
If you shared a pre-compiled .dll file, users can install it instantly without editing code:

Download the .dll file.

Open your ATAS custom indicators folder by pasting this path into your Windows File Explorer address bar:
%APPDATA%\ATAS\Indicators

Drop the .dll file directly into that folder.

Open or restart ATAS, open any chart, and press Ctrl + I.

Look under the Custom category to find and add Account Info(Custom).


Option B: Visual Studio
1. Create a New Class Library Project
Open Visual Studio and click Create a new project.

Search for and select Class Library (make sure it's the C# version targeting .NET Framework or the appropriate .NET runtime version your ATAS version uses, typically .NET 10 depending on the ATAS build). Click Next.

Name your project (e.g., AccountInfoCustom), choose your saving location, and click Create.

2. Add ATAS Reference Assemblies
To compile ATAS indicators, your project needs references to the core ATAS libraries (ATAS.Indicators.dll and OFT.Rendering.dll).

In the Solution Explorer on the right, right-click on Dependencies (or References) and select Add Reference... (or Manage NuGet Packages if applicable).

Click Browse and navigate to your ATAS installation directory (usually C:\Program Files\ATAS\ or your user path).

Select the following required DLL files:

ATAS.Indicators.dll

OFT.Rendering.dll

Any other dependencies referenced by your project (like data feed cores).

Click OK to add them.
(Tip: In the reference properties, set Copy Local to False since ATAS loads these natively at runtime).

3. Add the Code File
Visual Studio automatically creates a default file named Class1.cs. Right-click it, select Rename, and change it to MyCustomIndicator.cs.

Open the file, delete any placeholder code, and paste your indicator C# source code into it.

Save the file (Ctrl + S).

4. Build the Project
Go to the top menu and select Build > Clean Solution (to clear out old build caches).

Select Build > Build Solution (Ctrl + Shift + B).

Check the Output window at the bottom to ensure it says 1 succeeded, 0 failed.

5. Deploy to ATAS
Once built successfully, go to your project folder in Windows Explorer and find the compiled file located in bin\Debug\ or bin\Release\.

Copy the generated .dll file.

Drop it directly into your local ATAS indicators folder:
%APPDATA%\ATAS\Indicators

Open ATAS, open a chart, press Ctrl + I, and add your custom indicator from the list!

(If you have any trouble during this process, chatgpt, claude or gemini is your friend)
