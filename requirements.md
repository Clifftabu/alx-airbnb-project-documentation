# Backend Requirements for Airbnb Clone

 1. User Authentication

### API Endpoints
- `POST /api/register` - Register a new user
- `POST /api/login` - Authenticate and return JWT
- `GET /api/profile` - Get current user data (Auth required)

### Input/Output
- Input: `email`, `password`, `name`
- Output: JSON response with JWT or error

### Validation Rules
- Email must be unique
- Password must be at least 8 characters

### Performance Criteria
- Response within 300ms
- 99% availability



2. Property Management

### API Endpoints
- `POST /api/properties` - Create property (host only)
- `GET /api/properties` - List/search properties
- `PUT /api/properties/:id` - Edit listing
- `DELETE /api/properties/:id` - Delete listing

### Input/Output
- Input: `title`, `description`, `location`, `price`, `images`
- Output: Property object or list

### Validation Rules
- Title and price required
- Images must be valid URLs

### Performance Criteria
- Handle 1,000+ listings
- Paginate results



3. Booking System

### API Endpoints
- `POST /api/bookings` - Create booking
- `GET /api/bookings/:id` - View booking
- `DELETE /api/bookings/:id` - Cancel booking

### Input/Output
- Input: `property_id`, `check_in`, `check_out`
- Output: Booking details or error

### Validation Rules
- Check-in date must be in future
- Prevent double bookings

### Performance Criteria
- Real-time availability check
- 500ms or less response for booking request
