# 🤖 CryptoNode: A Full-Stack Trading Analysis Toolkit

> A professional-grade analysis toolkit for cryptocurrency traders, blending a Flutter mobile front-end with a data-intensive Python backend.

<img width="1280" height="1280" alt="CryptoNode" src="https://github.com/user-attachments/assets/3e5a943e-d799-4380-9713-d64f3e01ad1c" />


## ✨ Features

CryptoNode is built on three core pillars, designed to give traders a comprehensive edge in the market.

### 🤖 Bot Trader: Automated Signal Scanner

The backend bot constantly analyzes market conditions to find and deliver high-probability trade setups directly to your device.

* **Actionable Signals:** Provides a real-time feed of **long** and **short** signals for assets like `BTCUSDT`, `SOLUSDT`, and more.
* **Complete Trade Plan:** Every signal includes:
    * **Entry Price:** The suggested entry point for the trade.
    * **Stop Loss:** A calculated invalidation point to manage risk.
    * **Take Profit:** A target based on a minimum 3:1 Risk/Reward Ratio.
* **Clear Rationale:** Each signal is backed by a checklist of confirming factors, such as:
    * ✅ **HTF Trend Alignment:** The setup aligns with the dominant trend on the 4-hour chart.
    * ✅ **SMC Liquidity Sweep:** The entry is triggered after price sweeps a key liquidity zone.
    * ✅ **Confirmation Volume:** The entry candle shows a significant volume spike.

### ✅ Adaptive Validator: Your Personal Trading Coach

Stop guessing. Input your own trade ideas and let the validator analyze them against a sophisticated institutional trading thesis.

* **Institutional Thesis Analysis:** The validator checks your setup against a professional-grade model:
    * **Liquidity Grab:** Has a major swing high or low been convincingly swept?
    * **Market Structure Shift:** Has price broken a key level to confirm a change in direction?
    * **Point of Interest:** Is there a clean `Fair Value Gap (FVG)` that offers a high-probability entry?
* **Context-Aware Verdicts:**
    * **HIGH\_CONFIDENCE:** All institutional criteria are met.
    * **HIGH\_RISK\_COUNTER\_TREND:** The setup is valid but goes against the higher-timeframe trend.
    * **DAMAGE\_CONTROL:** Your active trade's thesis is broken; provides a plan to exit optimally.
* **Adaptive Profiles:** The analysis automatically adjusts timeframes based on your chosen profile: **Scalper**, **Day Trader**, or **Swing Trader**.

### 🔭 Coin Explorer: 360-Degree Market View

Get a deep, data-rich overview of any crypto asset, moving beyond simple price charts.

* **Top Movers Dashboard:** The initial screen immediately displays the day's top 5 gainers and top 5 losers in the futures market.
* **Detailed Asset Analysis:** A search for any symbol provides a multi-section report:
    * **Market Stats:** 24-hour high, low, and turnover volume.
    * **Live Order Book:** Best bid/ask prices and the current spread.
    * **Technical Indicators (1H):** A snapshot of key metrics like RSI, MACD, SMA/EMA, and Bollinger Bands.

---

## 📱 UI & User Experience

A clean, responsive, and intuitive interface designed for traders.

#### 🎨 Customizable Theming:

* **Dark Mode:** A sleek, GitHub-inspired dark theme (`#0D1117`) for focused, low-light analysis.
* **Light Mode:** A clean and professional light theme.

#### ✨ Polished Interface:

* `google_fonts` for beautiful, readable typography.
* `animate_do` for smooth, subtle animations that enhance the user experience.
* `iconsax` for a clean and modern set of icons.

#### 📖 Onboarding & Settings:

* A guided tour introduces new users to the three core features on their first launch.
* Settings are persisted locally using `shared_preferences`.

#### 🔄 Asynchronous Data Handling:

* Non-blocking UI with `FutureBuilder` to show loading spinners and handle API errors gracefully.
* Built-in `connectivity_plus` check to alert users of no internet connection.

---

## 🛠️ Technical Stack

### **Frontend (Flutter App)**

* **Framework:** `Flutter 3.x` with `Dart SDK >=3.0.0`
* **State Management:** `provider` - For theme management and separation of UI and logic.
* **API Communication:** `http`, `connectivity_plus` - For robust, asynchronous data fetching.
* **UI & UX:**
    * `google_fonts`: For custom, professional typography.
    * `animate_do`: For declarative and easy-to-implement animations.
    * `iconsax`: For a clean and modern icon library.
* **Local Storage:** `shared_preferences` - To save user settings like theme choice.

### **Backend (Python API)**

* **Framework:** `FastAPI` - For building high-performance, asynchronous APIs.
* **Data Analysis:**
    * `Pandas`: The core library for all data manipulation and time-series analysis.
    * `pandas_ta`: A powerful extension for calculating hundreds of technical indicators.
* **API Client:** `requests` - For interacting with the public Binance API.

---

## 🏛️ Architecture & Design

* **Full-Stack Architecture:** A clear separation of concerns with a powerful Python backend serving a Flutter mobile client via a REST API.
* **Service-Oriented Backend:** Logic is modularized into distinct services:
    * `api_client.py`: Handles all external communication with the Binance API.
    * `indicators.py`: A comprehensive, standalone library for all technical calculations.
    * `validator/logic.py` & `bot_trader/logic.py`: Encapsulated business logic for the core features.
* **Asynchronous & Non-Blocking:** The API uses `async/await` for high throughput, and the Flutter app uses `FutureBuilder` to ensure a smooth, responsive UI even while fetching large amounts of data.

---

## 💡 About the Project

As a developer with a passion for trading and financial markets, I created this project to:

* **Bridge the Gap:** Build tools that bring institutional-grade trading concepts (like Smart Money Concepts) to a wider audience in an accessible, automated way.
* **Showcase Full-Stack Skills:** Demonstrate proficiency in building a complete system from the ground up, combining a cross-platform mobile app (Flutter) with a high-performance, data-intensive backend (Python/FastAPI).
* **Combine Creative & Technical:** Merge the strategic thinking of trading with the technical implementation of modern software development.
