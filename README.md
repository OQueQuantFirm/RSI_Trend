### Prerequisites:


1. **Python & Anaconda Installation:**
   - Make sure you have Python installed on your Windows machine. You can download it from [python.org](https://www.python.org/downloads/windows/).
   - During installation, check the option to add Python to your system PATH.
   - Download Anaconda for Windows from [https://www.anaconda.com/products/distribution](https://www.anaconda.com/products/distribution).
   - Follow the installation instructions provided on the website.

2. **Git Installation:**
   - Install Git for Windows from [git-scm.com](https://git-scm.com/download/win).

### Setting up the Project:

3. **Clone the Repository:**
   - Open a command prompt or Git Bash.
   - Navigate to the directory where you want to clone the repository.
   - Run the following command:
     ```bash
     git clone https://github.com/OQueQuantFirm/RSI_Trend.git
     ```

4. **Install Required Libraries:**
   - Navigate to the project directory:
     ```bash
     cd RSI_Trend
     ```
   - Install the required Python libraries:
     ```bash
     pip install ccxt numpy pandas finta python-dotenv
     ```

5. **Create Environment Variables:**
   - Rename example.env to `.env` in the project directory.
   - Add the following lines to the `.env` file, replacing placeholders with your KuCoin Futures API credentials:
     ```plaintext
     API_KEY=your_api_key
     SECRET_KEY=your_secret_key
     PASSPHRASE=your_passphrase
     ```

### Step 6: Run the Notebook

   - In the Jupyter Notebook, run the cells.

   - Ensure that the required libraries are imported without any errors.

   - The code will run, fetch data, analyze the order book, and log results.


7. **Monitor Output:**
   - The program will print order book analysis results and trading signals to the console.
   - Check the logs in the `btc_rsi_trend.log` file for detailed information.


# RSI Trend Analysis with Order Book Imbalance

This guide explains how to use the provided Python code to perform Relative Strength Index (RSI) trend analysis with order book imbalance on the KuCoin Futures exchange. The code is designed to analyze the order book, calculate RSI, and generate trading signals based on certain conditions. Additionally, it allows you to customize symbols and timeframes for analysis.

### Code Customization

Open the provided Python script (`Tradin_V1.0.ipynb`) and follow the instructions below to customize the code:

# Call execute_order_book_analysis directly for your single symbol analysis, the code is located at the bottom

   ```python
   symbol_to_analyze = 'BTC/USDT:USDT'
   leverage = 10  # Define your desired leverage
   amount = 1  # Define your desired amount
   execute_order_book_analysis(symbol_to_analyze, leverage, amount)
   ```

1. **Symbol and Timeframe**: Set the `symbol_to_analyze` variable to the trading pair you want to analyze, and adjust the timeframe by modifying the `ohlcv_data = self.exchange.fetch_ohlcv(symbol, '15m')` line.

   ```python
   symbol_to_analyze = 'YOUR_SYMBOL_HERE'  # Example: 'BTC/USDT:USDT'
   ```

2. **Leverage and Amount**: Set the leverage and trading amount according to your preferences.

   ```python
   leverage = 10  # Example: 10X leverage
   amount = 5   # Example: 5 units of trading token
   ```

3. **Take Profit and Stop Loss Percentages**: Define the take profit and stop loss percentages.

   ```python
   TAKE_PROFIT_PERCENTAGE = 1.35   # Example: 13.5%
   STOP_LOSS_PERCENTAGE = 1.35    # Example: 13.5%
   ```

4. **Logging and CSV File**: Customize the logging configuration and CSV file settings if needed.

   ```python
   log_file_path = 'btc_rsi_trend.log'  # Specify the log file path by changing the symbol name
   ```

   ```python
   file_path = "btc_rsi_trend.csv"  # Specify the CSV file path by changing the symbol name
   ```

The script will continuously fetch OHLCV data, analyze the order book, and generate trading signals based on RSI and order book imbalance.

## Additional Notes

- The code utilizes the [CCXT](https://github.com/ccxt/ccxt) library for interacting with the KuCoin Futures API.

- The script is designed to run in a loop, fetching and analyzing data every 2 minutes (adjustable in the `time.sleep(120)` line).

Feel free to experiment with different symbols, timeframes, and parameters to adapt the code to your trading preferences.

### Notes:
- Ensure your API keys have the necessary permissions and are funded for trading.
- Always be cautious when running trading programs, especially with real funds.
- Periodically check for updates to libraries and the repository.

