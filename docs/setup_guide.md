# Options IV Dashboard - Setup Guide

This guide will help you set up and run the Options IV Dashboard Flask application.

## Prerequisites

- Python 3.x installed on your system
- pip (Python package installer)
- Git (for cloning the repository)

## Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/OptionsIV-Dashboard.git
   cd OptionsIV-Dashboard
   ```

2. **Create a Virtual Environment (Recommended)**
   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate

   # Linux/Mac
   python -m venv venv
   source venv/bin/activate
   ```

3. **Install Required Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure API Keys**
   - Navigate to `algoDashboard/keys.py`
   - Update the following credentials:
     ```python
     api_key = "YOUR_API_KEY"
     client_code = "YOUR_CLIENT_CODE"
     # Add other required credentials
     ```

5. **Set Up Data Directories**
   - The application will automatically create required directories:
     - `data/IVjsons/` - for storing JSON files
     - `logs/` - for application logs

## Running the Application

1. **Start the Flask Server**
   ```bash
   cd algoDashboard
   python app.py
   ```

2. **Access the Dashboard**
   - Open your web browser
   - Navigate to `http://localhost:5000`
   - You should see the Options IV Dashboard interface

## Application Structure

```
OptionsIV-Dashboard/
├── algoDashboard/
│   ├── app.py           # Main Flask application
│   ├── keys.py          # API credentials configuration
│   ├── data/            # Data storage
│   ├── static/          # CSS and other static files
│   └── templates/       # HTML templates
├── docs/
│   └── setup_guide.md   # This guide
└── requirements.txt     # Project dependencies
```

## Troubleshooting

1. **Missing Dependencies**
   - If you encounter any missing module errors, run:
     ```bash
     pip install -r requirements.txt
     ```

2. **API Connection Issues**
   - Verify your API credentials in `keys.py`
   - Check your internet connection
   - Ensure your API key has the necessary permissions

3. **Data Directory Issues**
   - The application will create necessary directories automatically
   - Ensure you have write permissions in the application directory

## Support and Resources

- Check the project's GitHub repository for updates
- Submit issues on GitHub for bug reports
- Refer to the documentation for API usage details

## Maintenance

- Regularly update dependencies using:
  ```bash
  pip install --upgrade -r requirements.txt
  ```
- Monitor the logs in the `logs/` directory for any issues
- Backup your API credentials and data periodically

## Security Notes

- Never commit your API credentials to version control
- Keep your virtual environment and dependencies updated
- Regularly monitor application logs for unusual activity