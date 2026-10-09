# Weather Dashboard

A full-stack weather dashboard with real-time data from OpenWeatherMap API. Features web and mobile apps with current weather, hourly forecast, 7-day forecast, and interactive maps.

## Project Structure

```
weather-dashboard/
├── backend/              # Node.js/Express API
├── frontend-web/         # React web application
├── mobile-app/          # React Native mobile app
├── docker-compose.yml   # Docker configuration
└── README.md
```

## Features

✅ Real-time weather data from OpenWeatherMap API
✅ Current weather display (temperature, humidity, wind speed, UV index)
✅ Hourly forecast (24 hours)
✅ 7-day weather forecast
✅ Interactive weather maps
✅ City search and geolocation
✅ Weather alerts and notifications
✅ Multiple units (Celsius/Fahrenheit, km/h/mph)
✅ Dark/Light theme
✅ Responsive design (web + mobile)
✅ Offline support with caching

## Tech Stack

### Backend
- Node.js with Express
- OpenWeatherMap API integration
- Redis caching
- JWT authentication
- PostgreSQL database

### Frontend Web
- React 18
- Redux Toolkit
- Tailwind CSS
- Recharts for data visualization
- Leaflet for maps

### Mobile App
- React Native with Expo
- React Navigation
- Redux Toolkit
- AsyncStorage for caching
- Geolocation services

## Getting Started

### Prerequisites
- Node.js v16+
- npm or yarn
- OpenWeatherMap API key (free tier available)
- Docker (optional)

### Installation

1. Clone the repository
```bash
git clone https://github.com/Anny7770/weather-dashboard.git
cd weather-dashboard
```

2. Backend setup
```bash
cd backend
npm install
cp .env.example .env
# Add your OpenWeatherMap API key to .env
npm start
```

3. Frontend Web setup
```bash
cd frontend-web
npm install
npm start
```

4. Mobile App setup
```bash
cd mobile-app
npm install
npm start
```

## Environment Variables

### Backend
```
PORT=5000
OPENWEATHER_API_KEY=your_api_key_here
DATABASE_URL=postgresql://user:password@localhost:5432/weather
REDIS_URL=redis://localhost:6379
JWT_SECRET=your_jwt_secret
NODE_ENV=development
```

## API Endpoints

- `GET /api/weather/current?city=London` - Current weather
- `GET /api/weather/forecast?lat=51.51&lon=-0.13` - 7-day forecast
- `GET /api/weather/hourly?city=London` - Hourly forecast
- `GET /api/alerts?city=London` - Weather alerts
- `POST /api/favorites` - Save favorite cities
- `GET /api/favorites` - Get favorite cities

## Deployment

### Docker
```bash
docker-compose up -d
```

### Heroku
```bash
heroku create your-app-name
git push heroku main
```

## License

MIT License - feel free to use this project

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
