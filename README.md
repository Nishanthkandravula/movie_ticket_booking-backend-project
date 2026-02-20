# Movie Ticket Booking Backend

🎬 A **REST API-based backend service** for booking movie tickets with user authentication, seat management, and payment integration.

## Features

- **User Authentication** – Sign up, login, password management
- **Movie Catalog** – Browse movies, shows, and timings
- **Seat Selection** – Real-time availability and seat booking
- **Booking Management** – Create, view, and cancel bookings
- **Payment Integration** – Mock payment gateway for transactions
- **Admin Panel** – Movie & show management

## Tech Stack

| Category | Tech |
|----------|------|
| **Language** | Java 8+ |
| **Framework** | Spring Boot |
| **Database** | MySQL |
| **APIs** | REST APIs |
| **Build Tool** | Maven |
| **Testing** | JUnit, Mockito |

## Getting Started

### Prerequisites
- Java 8 or higher
- Maven 3.6+
- MySQL 5.7+
- Postman (for testing APIs)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Nishanthkandravula/movie_ticket_booking-backend-project.git
   cd movie_ticket_booking-backend-project
   ```

2. **Configure MySQL**
   - Create a new MySQL database
   - Update `application.properties` with your credentials:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/movie_booking
     spring.datasource.username=root
     spring.datasource.password=your_password
     ```

3. **Build and Run**
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

4. **Access the API**
   - Server runs on: `http://localhost:8080`
   - API endpoints available at: `/api/v1/*`

## API Endpoints

### User Management
- `POST /api/v1/users/signup` – Register new user
- `POST /api/v1/users/login` – User login
- `GET /api/v1/users/{id}` – Get user details

### Movies & Shows
- `GET /api/v1/movies` – List all movies
- `GET /api/v1/shows/{movieId}` – Get shows for a movie
- `GET /api/v1/shows/{showId}/seats` – Get available seats

### Booking
- `POST /api/v1/bookings` – Create new booking
- `GET /api/v1/bookings/{userId}` – User's bookings
- `DELETE /api/v1/bookings/{bookingId}` – Cancel booking

## Testing

Run unit tests with Maven:
```bash
mvn test
```

Import `Movie_Booking_API.postman_collection.json` in Postman for API testing.

## Project Structure

```
src/
├── config/          # Configuration classes
├── models/          # Entity classes
├── repositories/    # Database access layer
├── services/        # Business logic
├── controllers/     # REST endpoints
├── exceptions/      # Custom exceptions
└── utils/           # Utility classes
```

## Future Enhancements

- 🔐 JWT token-based authentication
- 📧 Email notifications for bookings
- ⭐ User ratings and reviews
- 🎟️ Coupon and discount system
- 📊 Admin analytics dashboard
- 🔍 Search and filter improvements

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for bugs and feature requests.

## License

This project is open source and available under the MIT License.

---

**Built by** [Nishanth Kandravula](https://github.com/Nishanthkandravula)  
**Questions?** Reach out at kandravula.nishant@gmail.com
