## LangChain-French-Election-Analysis

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![Google AI](https://img.shields.io/badge/Google%20AI-4285F4?style=flat&logo=google&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-000000?style=flat&logo=chainlink&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=flat&logo=apache&logoColor=white)

A Python tool that converts CSV election data into a queryable SQLite database and lets you ask questions about voting patterns using natural language.

## What it does

**Input**: `resultats-definitifs-par-regions.csv` (French election results)  
**Output**: SQL database + AI-powered query interface + visualizations

Ask questions like:
- "How many people voted for Rassemblement National?"
- "Which region had the highest turnout?"
- "Show me vote distribution by party"

The system generates SQL queries automatically and returns answers with charts.

## Quick Start

```bash
# 1. Install dependencies
pip install pandas sqlite3 google-generativeai langchain-google-genai python-dotenv matplotlib

# 2. Add your Google API key
echo "GOOGLE_API_KEY=your_key_here" > .env

# 3. Place your CSV file in the project directory
# File must be named: resultats-definitifs-par-regions.csv

# 4. Run the notebook
jupyter notebook
```

## Core Files

- **Main notebook**: Data processing + query interface
- **CSV data**: `resultats-definitifs-par-regions.csv` (election results)
- **Database**: Auto-generated SQLite file
- **Config**: `.env` (API key storage)

## Technical Stack

- **Database**: SQLite (converted from CSV)
- **AI**: Google Gemini (query generation)
- **Framework**: LangChain (agent orchestration)
- **Analysis**: Pandas + Python REPL
- **Visualization**: Matplotlib

## Example Queries

```
"Total voters in France"
→ Generates: SELECT SUM(voters) FROM election_data

"Top 3 parties by votes" 
→ Returns ranked list with vote counts

"Regional breakdown for Marine Le Pen's party"
→ Creates regional comparison chart
```

## Data Structure

The CSV contains columns like:
- Region names
- Party vote counts
- Total registered voters
- Turnout percentages

Gets converted to normalized SQLite tables for efficient querying.

## Requirements

- Python 3.8+
- Google API key (for Gemini)
- French election CSV data file
- Internet connection (for AI queries)

## Installation

1. Clone or download this project
2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Create a `.env` file with your Google API key:
   ```
   GOOGLE_API_KEY=your_actual_api_key_here
   ```
4. Place your election data CSV file in the project directory
5. Open and run the Jupyter notebook

## Usage

1. Load the notebook in Jupyter
2. Run the data processing cells to convert CSV to SQLite
3. Use the natural language query interface to ask questions about the election data
4. View generated charts and analysis results

## Features

- ✅ Automatic CSV to SQLite conversion
- ✅ Natural language to SQL query generation
- ✅ Interactive data visualization
- ✅ Regional and party-based analysis
- ✅ Turnout and voting pattern insights
