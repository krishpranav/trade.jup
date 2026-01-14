# trade.jup:
Computer Vision–Based Trading Chart Analysis Engine
trade.jup is an experimental MVP that performs automated trading analysis directly from chart images using computer vision and quantitative techniques — without relying on market APIs, OHLC feeds, or broker integrations.
The system ingests real trading chart screenshots (candlestick or line charts) and extracts price structure from pixels to infer trends, support/resistance levels, volatility, and directional bias.

This project is designed as a research-grade foundation for next-generation discretionary and hybrid trading systems.

⸻

## Key Features:
	•	📷 Real Image Input
	•	Works on actual chart screenshots (TradingView, Binance, NSE, etc.)
	•	No mocked data, no synthetic OHLC
	•	🧠 Computer Vision–Driven Price Extraction
	•	Pixel-based price curve reconstruction
	•	Chart segmentation and noise reduction
	•	📊 Quantitative Market Analysis
	•	Trend estimation via regression
	•	Support & resistance detection
	•	Volatility proxy from price dynamics
	•	🧾 Explainable Trading Bias Output
	•	Human-readable market regime summary
	•	Directional bias (Long / Short / Range)
	•	Risk context based on volatility
	•	🧱 Standalone MVP
	•	Fully local execution
	•	No external APIs or services
	•	Jupyter Notebook–based for transparency and research

⸻

## Why trade.jup?:

Most trading tools assume structured market data.

trade.jup explores the opposite direction:

What if a machine could reason about markets the same way humans do — by looking at charts?

This approach is useful for:
	•	Discretionary trading augmentation
	•	Strategy validation from screenshots
	•	Markets with limited data access
	•	Research into vision-based financial intelligence

⸻

## Project Structure:

```
trade.jup/
├── data/
│   └── sample_chart.png        # Real chart image input
├── notebooks/
│   └── chart_analysis_mvp.ipynb
├── requirements.txt
├── README.md
└── venv/
```

⸻

## Environment Setup

### 1. Create virtual environment:
```
python3 -m venv venv
source venv/bin/activate
```

### 2. Install dependencies
```
pip install --upgrade pip
pip install -r requirements.txt
```

### 3. Install Tesseract OCR (required):

#### macOS:
```
brew install tesseract
```

#### Ubuntu:
```
sudo apt install tesseract-ocr
```

#### Windows:
```
	•	Download from: https://github.com/UB-Mannheim/tesseract/wiki
	•	Add install path to PATH
```

#### Verify:
```
tesseract --version
```

⸻

## Running the MVP

- Launch Jupyter Notebook:
```
jupyter notebook
```

- Open:
```
notebooks/chart_analysis_mvp.ipynb
```

- Place a real trading chart screenshot inside:
```
data/sample_chart.png
```
- Run the notebook top to bottom.

⸻

## Output Example

### The system produces:
	•	Extracted price curve from image
	•	Trend line overlay
	•	Support & resistance points
	•	Volatility estimate
	•	Final analysis summary, e.g.:

```
Trading Analysis Summary
------------------------
Trend           : Bullish Trend
Volatility      : High Volatility
Trend Slope     : 0.00421

Trading Bias
------------
Direction       : Long Bias
Risk Management : Reduce position size

```

⸻

## Current Limitations (MVP Scope):
	•	Price scale is relative (pixel-normalized)
	•	Candlestick body/wick parsing is basic
	•	No backtesting or order execution
	•	No live data ingestion

These are intentional to keep the MVP focused and interpretable.

⸻

##  Roadmap

Planned extensions include:
	•	Candlestick-level OHLC reconstruction
	•	CNN-based pattern recognition
	•	OCR-based absolute price extraction
	•	Multi-timeframe ensemble analysis
	•	Backtesting engine
	•	Desktop / web interface
	•	Real-time screen capture support

⸻

## Disclaimer

trade.jup is a research and educational project.

It does not provide financial advice and should not be used for live trading decisions without extensive validation, risk controls, and regulatory review.

⸻

## Project Status

Stage: MVP / Research Prototype
Focus: Vision-based market structure analysis
Audience: Quant researchers, ML engineers, system designers