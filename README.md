# 🧩 Online Sudoku Solver

An automated Python script that solves Sudoku puzzles from online websites using web scraping, backtracking algorithms, and browser automation.

## 🚀 Features

- **Automated Web Interaction**: Uses Selenium WebDriver to interact with online Sudoku websites
- **Intelligent Parsing**: Extracts Sudoku grids from web elements into Python matrices
- **Backtracking Algorithm**: Implements an efficient constraint satisfaction algorithm to solve puzzles
- **Auto-Input**: Automatically fills solved values back into the website
- **Continuous Operation**: Runs in a loop to solve multiple puzzles sequentially
- **Smart Validation**: Checks row, column, and 3×3 box constraints before placing numbers

## 🛠️ Technologies Used

- **Python 3.x**
- **Selenium WebDriver** - Browser automation
- **NumPy** - Matrix operations and mathematical computations
- **WebDriver Manager** - Automatic ChromeDriver management
- **Chrome Browser** - Headless browser automation

## 📋 Prerequisites

- Python 3.6 or higher
- Google Chrome browser installed
- Internet connection

## 🔧 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/online-sudoku-solver.git
   cd online-sudoku-solver
   ```

2. **Install required dependencies:**
   ```bash
   pip install selenium numpy webdriver-manager
   ```

3. **Ensure Chrome browser is installed** on your system.

## 🎯 Usage

1. **Run the solver:**
   ```bash
   python main.py
   ```

2. **The script will:**
   - Open Chrome browser automatically
   - Navigate to the Sudoku website
   - Extract the puzzle grid
   - Solve it using backtracking algorithm
   - Input the solution back into the website
   - Wait 15 seconds and repeat with a new puzzle

3. **To stop the program**, press `Ctrl+C` in the terminal.

## 🧠 How It Works

### Algorithm Overview

1. **Web Scraping**: The script uses Selenium to extract Sudoku grid values from HTML elements with IDs like `c_X_Y`
2. **Matrix Conversion**: Converts the scraped data into a 9×9 NumPy matrix
3. **Backtracking Solution**: 
   - Finds empty cells (value = 0)
   - Tries numbers 1-9 in each empty cell
   - Validates placement against Sudoku rules
   - Recursively solves remaining cells
   - Backtracks if no valid solution found
4. **Auto-Input**: Injects solved values back into the website using JavaScript execution

### Validation Logic

The solver ensures each number placement is valid by checking:
- **Row constraint**: Number doesn't already exist in the same row
- **Column constraint**: Number doesn't already exist in the same column  
- **Box constraint**: Number doesn't already exist in the same 3×3 sub-grid

## 🌐 Supported Websites

Currently configured for: `https://www.soduko-online.com/`

## ⚙️ Configuration

You can modify the following in `main.py`:
- **Target URL**: Change the `URL` variable to use different Sudoku websites
- **Timing**: Adjust the `time.sleep(15)` value to change puzzle refresh interval
- **Browser Options**: Modify Chrome options in the `opt` object

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

This tool is for educational purposes only. Please respect the terms of service of the websites you interact with and use responsibly.

## 🐛 Troubleshooting

**Chrome driver issues:**
- The script automatically downloads the correct ChromeDriver version
- Ensure Chrome browser is up to date

**Element not found errors:**
- Website structure may have changed
- Check if the target website is accessible
- Verify element IDs in the source code

**Slow performance:**
- Adjust sleep timers if needed
- Check internet connection stability

---

Made with ❤️ for Sudoku enthusiasts and automation lovers!
