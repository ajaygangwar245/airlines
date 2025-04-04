# Airlines Project

## Overview
This project is part of Harvard's CS50 Web Programming with Python and JavaScript, specifically for **Week 4: SQL, Models, and Migrations**. The project focuses on building a simple airline booking system using Django's ORM, models, and database migrations.

## Features
- Display available flights with origin, destination, and duration.
- View flight details, including passengers on board.
- Book a passenger onto a flight.
- Manage database migrations using Django ORM.

## Technologies Used
- Python
- Django
- SQLite (default Django database)
- HTML, CSS (for basic frontend)

## Setup Instructions
1. **Clone the repository**:
   ```sh
   git clone https://github.com/ajaygangwar245/airlines.git
   cd airlines-project
   ```
2. **Create a virtual environment and activate it**
  
3. **Install dependencies**
   
4. **Run migrations**:
   ```sh
   python manage.py migrate
   ```
5. **Load sample data (optional)**:
   ```sh
   python manage.py shell
   >>> from flights.models import Flight, Airport
   >>> jfk = Airport.objects.create(code="JFK", city="New York")
   >>> lax = Airport.objects.create(code="LAX", city="Los Angeles")
   >>> Flight.objects.create(origin=jfk, destination=lax, duration=300)
   >>> exit()
   ```
6. **Run the development server**:
   ```sh
   python manage.py runserver
   ```
7. Open [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser.

## Directory Structure
```
airline/
│-- airline/ 
│-- flights/            # Main app for flight management
│   │-- migrations/     # Database migrations
│   │-- templates/      # HTML templates
│   │-- views.py        # View logic
│   │-- models.py       # ORM models
│-- users/ 
│-- manage.py           # Django management script
│-- db.sqlite3          # SQLite database file
```

## Django Models
- **Airport**: Represents an airport with a code and city.
- **Flight**: Stores flight details like origin, destination, and duration.
- **Passenger**: Represents passengers who can book flights.

## Booking a Flight
1. Navigate to the homepage to see available flights.
2. Click on a flight to view details and passengers.
3. Enter passenger details to book a seat.

## Future Improvements
- Implement user authentication for booking.
- Enhance UI with Bootstrap or Tailwind.
- Use PostgreSQL instead of SQLite for production.

## License
This project is part of the CS50 Web course and follows its licensing terms.

---
**Author:** [@ajaygangwar245](https://github.com/ajaygangwar245)

For any issues or questions, feel free to open an issue on GitHub or contact me!