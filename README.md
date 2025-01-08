# 🌤️ Weather Data Collection System - DevOps Day 1 Challenge

## Project Overview
This project is a **Weather Data Collection System** that demonstrates core DevOps principles by combining:

- **External API Integration** (OpenWeather API)
- **Cloud Storage** (AWS S3)
- **Infrastructure as Code**
- **Version Control** (Git)
- **Python Development**
- **Error Handling**
- **Environment Management**

---

## 🎯 Features
- Fetches real-time weather data for multiple cities.
- Displays temperature (°F), humidity, and weather conditions.
- Automatically stores weather data in AWS S3.
- Supports tracking of multiple cities.
- Timestamps all data for historical tracking.

---

## 🛠️ Technical Architecture
### **Language**
- Python 3.x

### **Cloud Provider**
- AWS (S3)

### **External API**
- [OpenWeather API](https://openweathermap.org/api)

### **Dependencies**
- `boto3` (AWS SDK for Python)
- `python-dotenv` (for environment variable management)
- `requests` (for HTTP requests to the OpenWeather API)

---

## 🚀 How It Works
1. **Fetch Data**  
   The system uses the OpenWeather API to fetch real-time weather data for specified cities.

2. **Process Data**  
   Extracts and formats key weather details:
   - Temperature (°F)
   - Humidity
   - Weather Conditions

3. **Store Data**  
   Saves the weather data in JSON format to an AWS S3 bucket for further analysis.

4. **Repeatable & Scalable**  
   Designed for automation and scalability using Infrastructure as Code principles.

---

## 📋 Prerequisites
1. AWS Account with an S3 Bucket.
2. OpenWeather API Key.
3. Python 3.x installed locally.
4. Git for version control.

---

## 📂 Directory Structure
```plaintext
weather-dashboard/
├── .env               # Environment variables (e.g., API keys)
├── weather_data/      # Local storage for weather data
├── scripts/           # Python scripts for fetching and uploading data
│   ├── fetch_weather.py
│   └── upload_to_s3.py
├── requirements.txt   # Project dependencies
├── README.md          # Project documentation
└── config/            # Configuration files

🔧 Setup Instructions
Clone the Repository
git clone https://github.com/username/weather-dashboard.git
cd weather-dashboard

Install Dependencies
pip install -r requirements.txt

Configure Environment Variables
Create a .env file in the project root:
env
OPENWEATHER_API_KEY=your_openweather_api_key
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
S3_BUCKET_NAME=your_s3_bucket_name
Run the Script

python scripts/fetch_weather.py
python scripts/upload_to_s3.py
🌟 Example Output
{
    "city": "London",
    "temperature": 50.0,
    "humidity": 80,
    "weather_condition": "Cloudy",
    "timestamp": "2025-01-08T12:00:00Z"
}
🛡️ Error Handling
Invalid API key: Prompts user to check API key in .env.
Failed API requests: Logs error details for debugging.
AWS S3 issues: Handles permission errors and connectivity issues gracefully.
🖋️ Contributing
Feel free to fork the repository and submit pull requests to improve the system.

🤝 Acknowledgments
[OpenWeather API Keys](https://bit.ly/openweatherapi)
AWS
Python community for awesome libraries and tools.


