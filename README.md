# Automated Customer Feedback Sentiment Analyzer

## 🎯 Project Overview
An automated UiPath solution that analyzes customer feedback sentiment using text analytics. This project reads customer feedback from Excel files, performs sentiment analysis, and categorizes feedback as Positive, Negative, or Neutral.

## ✨ Features
- 📊 Excel file integration for input/output
- 🤖 Automated sentiment classification
- 📈 Real-time analytics and counting
- 💾 Results saved back to Excel with sentiment labels
- 📋 Summary statistics display

## 🔧 Prerequisites
- **UiPath Studio** (Version 2023.10 or higher)
- **Microsoft Excel** installed on your machine
- Required UiPath Packages:
  - UiPath.Excel.Activities (v2.20.0)
  - UiPath.System.Activities (v23.10.3)
  - UiPath.UIAutomation.Activities (v23.10.4)

## 📁 Project Structure
```
CustomerFeedbackSentimentAnalyzer/
├── .gitignore
├── README.md
├── project.json
├── Main.xaml
├── Data/
│   └── sample_feedback.xlsx
└── .local/
```

## 🚀 Installation & Setup

### Method 1: Clone from GitHub
```bash
git clone https://github.com/yourusername/CustomerFeedbackSentimentAnalyzer.git
cd CustomerFeedbackSentimentAnalyzer
```

### Method 2: Manual Setup
1. Create a new folder named `CustomerFeedbackSentimentAnalyzer`
2. Copy all project files into the folder
3. Open UiPath Studio
4. File → Open → Select the `project.json` file
5. Install dependencies when prompted

## 📊 Excel File Format
Your Excel file should have the following structure:

| Customer ID | Feedback | Sentiment |
|------------|----------|-----------|
| 1 | This product is amazing! | (will be filled) |
| 2 | Very poor quality | (will be filled) |
| 3 | It's okay | (will be filled) |

**Note:** The "Sentiment" column will be automatically populated by the bot.

## ▶️ How to Run
1. Open the project in UiPath Studio
2. Prepare your Excel file with customer feedback
3. Click **Run** or press **F5**
4. Enter the path to your Excel file when prompted
5. Wait for the analysis to complete
6. View the results summary

## 🎨 Workflow Description

### Main.xaml
The main workflow performs the following steps:
1. **Input Dialog** - Prompts user for Excel file path
2. **Read Excel** - Reads customer feedback data
3. **Sentiment Analysis** - Analyzes each feedback entry:
   - Positive keywords: good, great, excellent, love, amazing
   - Negative keywords: bad, poor, terrible, hate, worst
   - Neutral: Everything else
4. **Count Statistics** - Tracks positive, negative, and neutral counts
5. **Write Results** - Updates Excel with sentiment labels
6. **Display Summary** - Shows analysis results

## 🔍 Sentiment Classification Logic
The bot uses keyword-based sentiment analysis:
- **Positive**: Contains words like "good", "great", "excellent", "love", "amazing"
- **Negative**: Contains words like "bad", "poor", "terrible", "hate", "worst"
- **Neutral**: Doesn't contain strong positive or negative keywords

## 📈 Sample Output
After execution, you'll see:
```
Analysis Complete!

Positive: 45
Negative: 12
Neutral: 23
```

## 🛠️ Customization
You can extend this project by:
- Adding more sentiment keywords in the If conditions
- Integrating ML-based sentiment analysis APIs
- Adding data visualization
- Exporting results to different formats (CSV, PDF)
- Sending email notifications with results

## 🐛 Troubleshooting
| Issue | Solution |
|-------|----------|
| Excel file not found | Ensure the file path is correct and the file exists |
| Missing packages | Install packages via Manage Packages in UiPath Studio |
| Permission errors | Run UiPath Studio as Administrator |
| Excel is already open | Close Excel before running the bot |

## 📝 License
This project is open source and available under the MIT License.

## 👨‍💻 Author
Created for automated customer feedback analysis

## 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support
For issues or questions, please open an issue on GitHub.

---
**Made with ❤️ using UiPath**