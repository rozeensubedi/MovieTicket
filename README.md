Movie Hall Management System – Design & Requirements Explanation

System Objective:

To manage and streamline movie screenings, hall allocations, customer bookings, and seat availability in a cinema or multiplex environment.

System Design

1. Customer Management

- The system must store details of customers who make bookings.

- Data Stored:

  - First name, Last name

  - Email and phone number

- Requirement:

  - Each customer must have a unique identifier.

  - A customer can book multiple screenings.

2. Movie Management
   
- The system maintains information about movies being screened.

- Data Stored:

  - Movie title, genre, duration, release year, rating

- Requirement:

  - Each movie is uniquely identified.

  - A movie can be screened multiple times, across different halls and times.

3. Hall Management
   
The system manages the details of movie halls.

- Data Stored:

  - Hall name and total seat count

- Requirement:

  - Each hall must be uniquely identified.

  - A hall can host different screenings (at different times).

4. Screening Schedule Management
   
- The system handles scheduling of movies in specific halls at specific times.

- Data Stored:

  - Movie, hall, and screening date & time

- Requirement:

  - A screening must reference a specific movie and hall.

  - Avoid scheduling conflicts in the same hall.

5. Booking Management
   
- The system facilitates booking of seats for a particular screening by customers.

- Data Stored:

  - Customer ID, Screening ID, number of seats booked, booking timestamp

- Requirement:

  - A booking must be associated with a valid screening and customer.

  - Seats booked must not exceed the hall’s seat limit.

  - The system should allow for multiple bookings per screening.

Relationships & Flow:

1. A customer books a screening.

2. A screening is a combination of a movie shown in a hall at a specific time.

3. A hall contains a defined number of seats.

4. The system ensures:

  - No double bookings for the same seat/time

  - Screening conflicts are avoided

  - Real-time seat availability is updated

Business Rules & Constraints:

- A screening cannot be created without assigning a movie and hall.

- Booking cannot proceed if the number of requested seats exceeds availability.

- Customers must provide valid contact information.
