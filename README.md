# Space Explorer CLI 🚀

A Node.js command-line application that integrates with publicly available space-related APIs to provide real-time information about astronomical pictures, the International Space Station (ISS) location, and upcoming space launches.

## 🌟 Features

- **NASA Astronomy Picture of the Day**: Get daily astronomical images with detailed explanations
- **ISS Location Tracker**: Real-time tracking of the International Space Station's position
- **Upcoming Launches**: Browse and filter upcoming space launches worldwide

## 🛠️ Installation

1. Clone the repository:
```bash
git clone https://github.com/YahiaSharabasWSB/space-explorer-cli.git
cd space-explorer-cli
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.example .env
```

4. Get your NASA API key from [https://api.nasa.gov/](https://api.nasa.gov/) and add it to your `.env` file:
```
NASA_API_KEY=your_api_key_here
```

## 📖 Usage

### View NASA's Astronomy Picture of the Day
```bash
npm start apod
```

### Track the ISS location
```bash
npm start iss
```
Updates every 10 seconds. Press Ctrl+C to stop tracking.

### View upcoming space launches
```bash
npm start launches
```

Filter launches by status:
```bash
npm start launches --status active
```

Filter launches by days from now:
```bash
npm start launches --days 30
```

## 📁 Project Structure

```
space-explorer-cli/
├── index.js                 # Main entry point
├── services/               # API service modules
│   ├── nasaService.js     # NASA APOD API integration
│   ├── issService.js      # ISS location API integration
│   └── launchService.js   # Launch Library API integration
├── utils/                 # Utility functions
│   ├── displayUtils.js    # Display formatting utilities
│   └── dateUtils.js       # Date handling utilities
└── tests/                # Test files
    ├── nasaService.test.js
    ├── issService.test.js
    └── launchService.test.js
```

## 🧪 Testing

Run the test suite:
```bash
npm test
```

## 🌐 API Resources

- [NASA API (APOD)](https://api.nasa.gov/)
- [Open Notify ISS Location API](http://open-notify.org/Open-Notify-API/ISS-Location-Now/)
- [Launch Library 2 API](https://thespacedevs.com/llapi)

