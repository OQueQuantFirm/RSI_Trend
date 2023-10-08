### Prerequisites:
1. **Python Installation:**
   - Make sure you have Python installed on your Windows machine. You can download it from [python.org](https://www.python.org/downloads/).
   - During installation, check the option to add Python to your system PATH.

2. **Git Installation:**
   - Install Git for Windows from [git-scm.com](https://git-scm.com/download/win).

### Setting up the Project:

3. **Clone the Repository:**
   - Open a command prompt or Git Bash.
   - Navigate to the directory where you want to clone the repository.
   - Run the following command:
     ```bash
     git clone https://github.com/your-username/your-repository.git
     ```

4. **Install Required Libraries:**
   - Navigate to the project directory:
     ```bash
     cd your-repository
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

### Running the Program:

6. **Run the Python Script:**
   - Execute your Python script or Jupyter Notebook:
     ```bash
     python your_script.py
     ```
     or
     ```bash
     jupyter notebook your_notebook.ipynb
     ```

7. **Monitor Output:**
   - The program will print order book analysis results and trading signals to the console.
   - Check the logs in the `arb_rsi_trend.log` file for detailed information.

### Notes:
- Ensure your API keys have the necessary permissions and are funded for trading.
- Always be cautious when running trading programs, especially with real funds.
- Periodically check for updates to libraries and the repository.

By providing these instructions, users can easily set up and run your trading program on Windows. Additionally, you may want to include a disclaimer about the risks associated with trading and the importance of testing in a simulated environment before deploying with real funds.
# RSI_Trend
Order Book Imbalance analysis with RSI Trading Program for Kucoin Futures trading. 
