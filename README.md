# API Gateway

An NGINX-based API Gateway that provides routing, authentication, and request forwarding for the DolceIQ platform microservices.

## Features

- **Service Routing**: Routes requests to appropriate microservices based on URL patterns
- **JWT Authentication**: Validates tokens via User Service for protected endpoints
- **User Identification**: Forwards authenticated user IDs to downstream services
- **Request Proxying**: Handles request/response forwarding with proper headers
- **Load Balancing**: Upstream configuration for service load balancing
- **Security**: Protects sensitive endpoints behind authentication

## Architecture

### Service Routing

The gateway routes requests based on URL patterns:

- `/api/user/*` → User Service
- `/api/recipe/*` → Recipe Service
- `/_verify_token` → Internal endpoint for token verification
