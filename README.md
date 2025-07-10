
# 📈 Stock Predictions AI App

Welcome to the **Stock Predictions AI App** — a fast, fun, and slightly chaotic web application that blends real-time stock data with the unpredictable brilliance of AI-generated trading advice. Whether you're a casual investor, finance meme lover, or just here for the absurdity, this app delivers hot takes on hot stocks.

---

## 🎯 What It Does

- 🔍 Enter stock tickers like `AAPL`, `TSLA`, `NVDA`, and more.
- 📊 The app fetches the last 3 days of historical stock prices using the [Polygon.io](https://polygon.io/) API.
- 🧠 Data is sent to an AI (via OpenAI API), which generates a 150-word report filled with dramatic flair and financial sass.
- 😂 The report is designed to entertain while mimicking (but not replacing!) market commentary.
- ⚡ Uses Cloudflare Workers to securely handle API calls and avoid CORS issues.

---

## 🛠️ Tech Stack

- **Frontend**: HTML, CSS, JavaScript (Vanilla)
- **Serverless Backend**: Cloudflare Workers
- **Data Source**: [Polygon.io](https://polygon.io/)
- **AI Integration**: OpenAI GPT-based model

---

## 🚀 How to Use It

### 🔧 Prerequisites

1. A **Polygon.io API Key** – get one at [polygon.io](https://polygon.io/)
2. An **OpenAI API Key** – get one at [openai.com](https://platform.openai.com/)

### 🔨 Clone the Repository

```bash
git clone https://github.com/niksom406/Stock-Prediction-AI-App.git
cd Stock-Prediction-AI-App
```

---

## 🧠 How It Works

1. User enters one or more stock tickers (e.g., `GOOGL`, `META`).
2. A frontend button triggers a call to a **Polygon API Worker** which fetches 3 days of price data.
3. This data is compiled and sent to an **OpenAI Worker**.
4. The AI uses example prompts to generate a fun stock report.
5. The result is rendered in the browser.

---

## 🧪 Deployment

You will need to deploy **two Cloudflare Workers**:

### 🔹 1. Polygon API Worker

Wraps the Polygon.io API with CORS headers.

```js
// Add to environment variables in the Cloudflare dashboard:
POLYGON_API_KEY=<your_polygon_api_key>
```

### 🔹 2. OpenAI API Worker

Wraps the OpenAI chat completion endpoint.

```js
// Add to environment variables in the Cloudflare dashboard:
OPENAI_API_KEY=<your_openai_api_key>
```

> Both workers use simple `fetch()` proxies with CORS support and custom headers.

---

## 💻 Local Development

To test locally, serve the static HTML page with any local server:

```bash
npx serve .
```

Or open `index.html` directly in your browser (CORS restrictions may apply if your workers aren’t deployed yet).

---

## 📸 Screenshots

### 📊 App Interface
![UI Screenshot](./app_interface.png)

---

## 💬 Example AI Report

> OK baby, hold on tight! You are going to haate this! Over the past three days, Tesla (TSLA) shares have plummetted. The stock opened at $223.98 and closed at $202.11 on the third day, with some jumping around in the meantime. This is a great time to buy, baby! But not a great time to sell!

> Apple (AAPL) stocks have gone stratospheric! This is a seriously hot stock right now. They opened at $166.38 and closed at $182.89 on day three. So all in all, I would hold on to Tesla shares tight if you already have them – they might bounce right back up and head to the stars!

---

## 🤯 Disclaimer

> **This app is for entertainment purposes only.**  
> It is not financial advice.  
> Do not make trades based on these reports unless you’re also consulting a trusted financial professional.  
> The AI has jokes — your wallet doesn’t.

---

## 🙌 Acknowledgments

- Inspired by the madness of the stock market and the brilliance of large language models.
- Built with ❤️ using:
  - [Polygon.io](https://polygon.io/)
  - [OpenAI](https://openai.com/)
  - [Cloudflare Workers](https://developers.cloudflare.com/workers/)
- UI and logic by [@niksom406](https://github.com/niksom406)

---

## 📬 Contact

Got questions? Suggestions? Want to collab or roast the AI's stock takes?

Open an [issue](https://github.com/niksom406/Stock-Prediction-AI-App/issues)  
Or message [@niksom406](https://github.com/niksom406)
