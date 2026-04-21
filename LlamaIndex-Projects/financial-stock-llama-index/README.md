# Financial Stock Analysis using LlamaIndex

An AI-powered financial analysis tool that queries indexed stock data to generate reports on individual stocks or competitor comparisons. Built with LlamaIndex and OpenAI.

## Tech Stack

- **Python** — application logic
- **LlamaIndex** — document indexing and query engine
- **OpenAI** — GPT model for report generation
- **Streamlit** — web UI
- **IB Insync** — Interactive Brokers API for fetching stock data

## Supported Stocks

`MSFT` · `NVDA` · `GOOG` · `META` · `AAPL` · `TSM`

---

## How to Run

### Step 1 — Create and activate a conda environment

```bash
conda create -n finance python=3.10 -y
conda activate finance
```

### Step 2 — Install dependencies

```bash
pip install -r requirements.txt
```

### Step 3 — Set up environment variables

Copy `.env.example` to `.env` and fill in your key:

```bash
cp .env.example .env
```

```ini
OPENAI_API_KEY=your_openai_api_key_here
```

### Step 4 — Run the app

```bash
streamlit run app.py
```

Open [http://localhost:8501](http://localhost:8501) in your browser.

---

## Usage

Select a report type from the dropdown:

- **Single Stock Outlook** — enter a stock symbol (e.g. `AAPL`) to generate a 2023–2027 outlook report including risks and headwinds
- **Competitor Analysis** — enter two stock symbols (e.g. `MSFT` and `GOOG`) to generate a head-to-head competitive analysis

> **Note:** The app loads from a pre-built index in `./storage`. Make sure the storage directory exists and is populated before running.
