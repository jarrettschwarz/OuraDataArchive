# OuraDataArchive

Personal health data archiving tool for Oura Ring users. Export, backup, and analyze your Oura Ring data with customizable date ranges, multiple export formats, and long-term storage solutions.

## 🎯 Overview

OuraDataArchive helps Oura Ring users take control of their health data by providing:

- **Complete Data Export**: Download all your Oura Ring metrics including sleep, activity, readiness, heart rate, and more
- **Flexible Date Ranges**: Export specific time periods or your entire history
- **Multiple Formats**: Save data as CSV, JSON, or structured databases
- **Privacy-First**: Your data stays on your devices - no cloud storage required
- **Analysis Tools**: Built-in visualization and trend analysis capabilities
- **Backup Solutions**: Automated backup scheduling and data integrity verification

## 🚀 Features

### Data Export
- ✅ Sleep metrics (stages, efficiency, latency)
- ✅ Activity data (steps, calories, distance)
- ✅ Readiness scores and contributing factors
- ✅ Heart rate (resting, variability, intraday)
- ✅ Body temperature trends
- ✅ Workout sessions and performance
- ✅ Personal profile information

### Export Options
- **Time Ranges**: Last 30 days, custom dates, or complete history
- **File Formats**: CSV (Excel-compatible), JSON (developer-friendly), SQLite database
- **Batch Processing**: Export multiple data types simultaneously
- **Incremental Backups**: Only export new data since last backup

### Analysis & Visualization
- 📊 Sleep trend analysis
- 📈 Activity pattern recognition
- 🔄 HRV and readiness correlations
- 📅 Calendar heatmaps for long-term trends
- 📋 Automated health reports

## 🛠 Installation

### Prerequisites
- Python 3.7+
- Oura Ring (Gen 2, Gen 3, or Gen 4)
- Active Oura account

### Quick Start
```bash
git clone https://github.com/yourusername/OuraDataArchive.git
cd OuraDataArchive
pip install -r requirements.txt
python setup.py
```

### Configuration
1. Get your Oura Personal Access Token from [cloud.ouraring.com](https://cloud.ouraring.com)
2. Run the setup wizard: `python configure.py`
3. Start your first export: `python export.py`

## 📖 Usage

### Basic Export
```bash
# Export last 30 days of all data
python export.py --days 30 --format csv

# Export specific date range
python export.py --start 2024-01-01 --end 2024-01-31 --format json

# Export everything
python export.py --all --format sqlite
```

### Scheduled Backups
```bash
# Set up daily automated backups
python schedule.py --frequency daily --format csv --destination ./backups/
```

### Analysis
```bash
# Generate health trends report
python analyze.py --report trends --timeframe 90days

# Create visualization dashboard
python dashboard.py --port 8080
```

## 🔧 Configuration Options

### Export Settings
- **Data Types**: Choose which metrics to include
- **Date Ranges**: Flexible time period selection
- **File Organization**: Folder structure and naming conventions
- **Data Validation**: Integrity checks and error handling

### Privacy & Security
- **Local Storage**: All data processing happens on your device
- **Token Security**: Encrypted storage of API credentials
- **Data Retention**: Configurable automatic cleanup policies
- **Export Encryption**: Optional password protection for exports

## 📊 Supported Data Types

| Category | Metrics | API Endpoint |
|----------|---------|--------------|
| **Sleep** | Duration, efficiency, stages, latency | `/daily_sleep` |
| **Activity** | Steps, calories, distance, intensity | `/daily_activity` |
| **Readiness** | Score, HRV, temperature, recovery | `/daily_readiness` |
| **Heart Rate** | Resting, variability, intraday | `/heartrate` |
| **Workouts** | Sessions, intensity, duration | `/workout` |
| **Personal** | Profile, preferences, device info | `/personal_info` |

## 🔒 Privacy & Data Ownership

### Your Data, Your Control
- **No Cloud Dependencies**: Everything runs locally on your machine
- **Direct API Access**: Connect directly to Oura's official API
- **Transparent Processing**: Open source code you can audit
- **Easy Migration**: Standard formats work with any analysis tool

### Security Features
- Secure credential storage using system keychain
- Optional export encryption with AES-256
- No telemetry or usage tracking
- Regular security updates and vulnerability patches

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Setup
```bash
git clone https://github.com/yourusername/OuraDataArchive.git
cd OuraDataArchive
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements-dev.txt
pre-commit install
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

This tool is not affiliated with or endorsed by Oura Health. It uses Oura's official API and is intended for personal use only. Always consult healthcare professionals for medical advice.
