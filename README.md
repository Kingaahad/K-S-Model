# Enhanced KS Prediction Application

A modern, feature-rich application for KS prediction with advanced capabilities including machine learning, security, and user interface enhancements.

## Features

- Advanced machine learning model using EfficientNetB0
- Secure authentication and authorization
- Rate limiting and API protection
- Modern user interface with dark/light themes
- Real-time image processing
- Batch processing capabilities
- Comprehensive error tracking and monitoring
- Database migrations and versioning
- Extensive test coverage
- API documentation
- Performance monitoring
- Caching for improved performance

## Prerequisites

- Python 3.8 or higher
- Redis server
- SQLite database
- AWS account (optional, for S3 storage)

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd ks-prediction-app
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
```bash
cp .env.example .env
# Edit .env with your configuration
```

5. Initialize the database:
```bash
alembic upgrade head
```

## Configuration

The application can be configured through environment variables in the `.env` file:

- `DATABASE_URL`: Database connection string
- `REDIS_URL`: Redis connection string
- `SENTRY_DSN`: Sentry DSN for error tracking
- `AWS_ACCESS_KEY_ID`: AWS access key
- `AWS_SECRET_ACCESS_KEY`: AWS secret key
- `AWS_REGION`: AWS region
- `JWT_SECRET_KEY`: JWT secret key
- `ENCRYPTION_KEY`: Encryption key for sensitive data

## Usage

### Running the Application

1. Start the Redis server:
```bash
redis-server
```

2. Start the application:
```bash
python ks_prediction_app_enhanced.py
```

The application will be available at:
- Web UI: http://localhost:8000
- API: http://localhost:8000/api

### API Documentation

API documentation is available at http://localhost:8000/docs when the application is running.

### Testing

Run the test suite:
```bash
pytest tests/
```

Run tests with coverage:
```bash
pytest --cov=ks_prediction_app_enhanced tests/
```

## Security

- All passwords are hashed using bcrypt
- JWT tokens for authentication
- Rate limiting to prevent abuse
- Input validation and sanitization
- Secure session management
- Encryption for sensitive data

## Monitoring

The application includes:
- Prometheus metrics at /metrics
- Sentry error tracking
- Performance monitoring
- Resource usage tracking

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please open an issue in the repository or contact the maintainers.

## Acknowledgments

- TensorFlow team for the machine learning framework
- FastAPI team for the web framework
- Redis team for the caching solution
- SQLAlchemy team for the ORM
- All other open-source contributors 