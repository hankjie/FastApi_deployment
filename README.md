# FastAPI Deployment on Render

A simple FastAPI application ready for deployment on Render.

## Features

- Simple FastAPI application with basic endpoints
- CORS middleware enabled
- Health check endpoint
- Sample API endpoints for items

## Local Development

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run the application:
```bash
python main.py
```

3. Visit `http://localhost:8000` to see the API

## API Endpoints

- `GET /` - Root endpoint with welcome message
- `GET /health` - Health check endpoint
- `GET /api/items` - Get sample items
- `POST /api/items` - Create a new item

## Deployment on Render

### Method 1: Using render.yaml (Recommended)

1. Push this code to a GitHub repository
2. Connect your GitHub account to Render
3. Create a new Web Service on Render
4. Select your repository
5. Render will automatically detect the `render.yaml` file and use those settings

### Method 2: Manual Configuration

If you prefer to configure manually:

1. **Build Command**: `pip install -r requirements.txt`
2. **Start Command**: `python main.py`
3. **Environment**: Python 3
4. **Plan**: Free tier

## Environment Variables

The application uses the `PORT` environment variable (automatically set by Render) to determine which port to run on.

## Documentation

Once deployed, you can access the interactive API documentation at:
- Swagger UI: `https://your-app-name.onrender.com/docs`
- ReDoc: `https://your-app-name.onrender.com/redoc`
