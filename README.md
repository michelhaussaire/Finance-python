# Python Finance - Financial Analysis Toolkit

A comprehensive collection of Jupyter notebooks for financial analysis, including portfolio management, technical analysis, and trading strategy backtesting. This toolkit provides practical implementations of modern financial analysis techniques using Python.

## 📁 File Descriptions

### `test_portfolio.ipynb`
**Portfolio Analysis and Management**

This notebook implements an interactive Streamlit application for comprehensive investment portfolio analysis. Key features include:

- **Data Input Interface**: User-friendly input for financial assets (e.g., AAPL, MSFT, GOOGL, BTC) and analysis date selection
- **Data Acquisition**: Leverages `yfinance` API to retrieve historical adjusted closing prices
- **Return Calculations**: 
  - Daily portfolio returns computation
  - Cumulative returns analysis
  - Benchmark comparison against S&P 500 index
- **Risk Assessment**: Portfolio volatility calculation using covariance matrix methodology
- **Data Visualization**: 
  - Comparative performance charts (Portfolio vs S&P 500)
  - Portfolio composition pie charts with equal weighting
- **Risk Metrics**: Portfolio risk analysis compared to benchmark volatility

### `test_tradingview_ta.ipynb`
**Automated Technical Analysis with TradingView**

This notebook demonstrates the integration of `tradingview_ta` library for automated technical analysis:

- **Analysis Configuration**: Connects to TradingView API for specific symbol analysis (example: 'X' symbol on NYSE)
- **Technical Indicators**: Comprehensive indicator suite including:
  - RSI (Relative Strength Index)
  - Stochastic Oscillators (Stoch.K, Stoch.D)
  - CCI (Commodity Channel Index)
  - ADX (Average Directional Index)
  - MACD (Moving Average Convergence Divergence)
  - Moving Averages (EMA, SMA across multiple timeframes)
  - Bollinger Bands
  - Pivot Points (Classic, Fibonacci, Camarilla, Woodie, Demark)
- **Trading Recommendations**: Automated buy/sell recommendations based on technical analysis
- **Executive Summary**: Consolidated recommendation output (BUY/SELL/NEUTRAL) with signal distribution

### `test_backtesting.ipynb`
**Trading Strategy Backtesting Framework**

This notebook implements and validates trading strategies using the `backtesting` library:

- **Strategy Implementation**: SMACross (Simple Moving Average Crossover)
  - Short-term MA: 50 periods
  - Long-term MA: 100 periods
  - Buy signal: Short MA crosses above Long MA
  - Sell signal: Long MA crosses above Short MA

- **Backtest Configuration**:
  - Initial capital: $10,000
  - Commission structure: 0.2%
  - Dataset: SPY ETF from 2018-01-01

- **Performance Metrics**:
  - Total and annualized returns
  - Volatility and risk-adjusted ratios (Sharpe, Sortino)
  - Maximum and average drawdown analysis
  - Trade statistics and win rate
  - Profit factor and expectancy calculations

- **Parameter Optimization**: Automated optimization for optimal moving average parameters
- **Interactive Visualization**: Bokeh-powered interactive charts featuring:
  - Equity curve evolution
  - Entry/exit point markers
  - Technical indicator overlays
  - Drawdown period analysis

## 🛠️ Technology Stack

- **Python**: Core programming language
- **yfinance**: Yahoo Finance API wrapper for financial data
- **pandas**: Data manipulation and analysis framework
- **matplotlib**: Static data visualization library
- **streamlit**: Web application framework for interactive dashboards
- **tradingview_ta**: TradingView technical analysis integration
- **backtesting**: Vectorized backtesting framework
- **ta**: Technical analysis indicator library
- **bokeh**: Interactive visualization library
- **numpy**: Numerical computing foundation

## 🚀 Getting Started

### Prerequisites
```bash
pip install yfinance pandas matplotlib streamlit tradingview_ta backtesting ta bokeh numpy
```

### Usage Instructions

1. **Jupyter Notebook Execution**:
   ```bash
   jupyter lab
   # Navigate to desired .ipynb file and execute cells sequentially
   ```

2. **Streamlit Portfolio Analysis**:
   ```bash
   # Convert notebook to .py file first, then:
   streamlit run portfolio_app.py
   ```

3. **Command Line Backtesting**:
   ```python
   # Execute backtesting notebook cells or import as module
   from test_backtesting import SMACross, run_backtest
   ```

## 📊 Use Cases

- **Portfolio Managers**: Risk assessment and performance attribution analysis
- **Quantitative Traders**: Strategy development and validation framework
- **Financial Analysts**: Rapid technical analysis and market screening
- **Academic Researchers**: Financial modeling and empirical analysis foundation
- **Finance Students**: Practical implementation of theoretical concepts
- **Retail Investors**: Personal portfolio optimization and strategy testing

## 🔮 Future Roadmap

### Short-term Enhancements (Next 3 months)
- [ ] **Advanced Portfolio Optimization**
  - Modern Portfolio Theory implementation
  - Efficient frontier calculation
  - Risk parity and factor-based allocation models
- [ ] **Enhanced Risk Management**
  - Value at Risk (VaR) calculations
  - Expected Shortfall (ES) metrics
  - Monte Carlo simulation framework
- [ ] **Extended Data Sources**
  - Alternative data integration (sentiment, economic indicators)
  - Cryptocurrency market data expansion
  - Real-time data streaming capabilities

### Medium-term Development (3-6 months)
- [ ] **Machine Learning Integration**
  - Predictive modeling for price movements
  - Feature engineering for technical indicators
  - Ensemble methods for signal generation
- [ ] **Advanced Strategy Framework**
  - Multi-asset strategy support
  - Options and derivatives backtesting
  - High-frequency trading simulation
- [ ] **Web Application Development**
  - Full-stack dashboard with user authentication
  - Cloud deployment (AWS/GCP/Azure)
  - Real-time portfolio monitoring

### Long-term Vision (6+ months)
- [ ] **Institutional Features**
  - Multi-portfolio management system
  - Compliance and regulatory reporting
  - Performance attribution analysis
- [ ] **API Development**
  - RESTful API for strategy execution
  - Webhook integration for automated trading
  - Third-party platform connectivity

## 🔧 Possible Implementations

### Technical Analysis Enhancements
- **Custom Indicator Development**: Build proprietary technical indicators
- **Pattern Recognition**: Automated chart pattern detection using computer vision
- **Sentiment Analysis**: Social media and news sentiment integration
- **Market Regime Detection**: Statistical methods for market state identification

### Portfolio Management Extensions
- **Factor Models**: Fama-French multi-factor model implementation
- **ESG Integration**: Environmental, Social, Governance scoring
- **Alternative Assets**: Real estate, commodities, and private equity analysis
- **Currency Hedging**: Multi-currency portfolio risk management

### Risk Management Modules
- **Stress Testing**: Historical and hypothetical scenario analysis
- **Correlation Analysis**: Dynamic correlation monitoring and alerts
- **Liquidity Risk**: Market impact and liquidity-adjusted returns
- **Credit Risk**: Counterparty risk assessment for fixed income

### Automation and Integration
- **Broker API Integration**: Automated order execution (Interactive Brokers, Alpaca)
- **Cloud Infrastructure**: Scalable computing for large-scale backtesting
- **Notification Systems**: Email/SMS alerts for strategy signals
- **Database Integration**: PostgreSQL/MongoDB for historical data storage

## 📈 Performance Considerations

- **Vectorized Operations**: Optimized pandas operations for large datasets
- **Memory Management**: Efficient data handling for extended historical periods
- **Parallel Processing**: Multi-core utilization for parameter optimization
- **Caching Strategies**: Redis integration for frequently accessed data

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines for:
- Code style and formatting standards
- Testing requirements and coverage expectations
- Documentation standards and examples
- Pull request and issue templates

## 📄 License

This project is provided as-is for educational and research purposes. Some code components may be derived from various open-source projects and tutorials. Please ensure compliance with original source licenses when using or redistributing any part of this code.

## ⚠️ Disclaimer

**IMPORTANT NOTICE:**

- This software is **strictly for educational and research purposes only**
- The code may contain **reused and adapted components** from various sources and tutorials
- **Past performance does not guarantee future results** in any financial market
- This toolkit is **not intended for live trading** or actual investment decisions
- **No financial advice is provided** - this is purely educational material
- Users are **solely responsible** for any use of this code and its outcomes
- **Always consult with qualified financial professionals** before making investment decisions
- The authors assume **no liability** for any financial losses incurred through use of this software
- Code is provided **without warranty** of any kind, express or implied
- Users should **verify all calculations** and logic before any practical application