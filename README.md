# Hotel Reservation System

## Overview
The Hotel Reservation System is a console-based Java application that provides functionalities for managing hotel reservations. It uses MySQL as the database for storing reservation details.

## Features
1. **Reserve a Room for Guest**: Add a new reservation by specifying the guest's name, room number, and contact number.
2. **View Existing Reservations**: View all reservations in a tabular format.
3. **Check Room Number of a Guest**: Retrieve the room number associated with a specific reservation ID and guest name.
4. **Update Reservation Details**: Modify the guest name, room number, and contact number for an existing reservation.
5. **Delete a Reservation**: Remove an existing reservation by its ID.
6. **Exit the System**: Exit the application gracefully with a thank-you message.

## Prerequisites
- **Java Development Kit (JDK)** (version 8 or above) i"m using JDK 17 version 
- **MySQL Server** installed and running
- **MySQL JDBC Driver**  download mysql j connector (link :- https://dev.mysql.com/downloads/connector/j/) (must be added to your project's classpath)

## Database Setup
1. Create a MySQL database named `hotelreservation_db`.
2. Create a `reservation` table using the following SQL schema:
   ```sql
   CREATE TABLE reservation (
       reserved_id INT AUTO_INCREMENT PRIMARY KEY,
       guest_name VARCHAR(255),
       room_number INT,
       contact_no VARCHAR(15),
       reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );
