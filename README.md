# Hotel Management System

This is a Java-based **Hotel Management System** that allows users to manage hotel reservations. The system connects to a MySQL database to store and retrieve reservation details. Users can perform operations such as reserving a room, viewing reservations, updating reservations, deleting reservations, and retrieving room numbers.

---

## Features

1. **Reserve a Room**: Add a new reservation with guest details, room number, and contact information.
2. **View Reservations**: Display all current reservations in a table format.
3. **Get Room Number**: Retrieve the room number for a specific reservation using the reservation ID and guest name.
4. **Update Reservations**: Modify existing reservation details (guest name, room number, contact number).
5. **Delete Reservations**: Remove a reservation from the system using the reservation ID.

---

## Prerequisites

Before running the project, ensure you have the following installed:

1. **Java Development Kit (JDK)**: Version 8 or higher.
2. **MySQL Database**: Install and set up MySQL on your system.
3. **MySQL Connector/J**: Add the MySQL JDBC driver to your project. You can download it from [here](https://dev.mysql.com/downloads/connector/j/).
4. **IDE**: Use an IDE like IntelliJ IDEA, Eclipse, or any other Java-supported IDE.

---

## Setup

1. **Database Setup**:
   - Create a MySQL database named `hotel_dp`.
   - Create a table named `reservations` using the following SQL query:

     ```sql
     CREATE TABLE reservations (
         reservation_id INT AUTO_INCREMENT PRIMARY KEY,
         guest_name VARCHAR(100) NOT NULL,
         room_number INT NOT NULL,
         contact_number VARCHAR(15) NOT NULL,
         reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
     );
     ```

2. **Configure Database Connection**:
   - Update the `url`, `username`, and `password` in the `HotelManagementSystem` class to match your MySQL database configuration.

     ```java
     private static final String url = "jdbc:mysql://localhost:3306/hotel_dp?characterEncoding=UTF-8";
     private static final String username = "root"; // Replace with your MySQL username
     private static final String password = "pragadesh2003"; // Replace with your MySQL password
     ```

3. **Add MySQL Connector/J**:
   - Add the MySQL JDBC driver (`mysql-connector-java-x.x.x.jar`) to your project's classpath.

4. **Run the Project**:
   - Compile and run the `HotelManagementSystem` class.

---

## Usage

1. **Main Menu**:
   - Upon running the program, you will see the main menu with the following options:
     ```
     HOTEL MANAGEMENT SYSTEM
     1. Reserve a room
     2. View Reservations
     3. Get Room Number
     4. Update Reservations
     5. Delete Reservations
     0. Exit
     ```

2. **Reserve a Room**:
   - Choose option `1` and provide the guest name, room number, and contact number to create a reservation.

3. **View Reservations**:
   - Choose option `2` to view all current reservations in a table format.

4. **Get Room Number**:
   - Choose option `3` and provide the reservation ID and guest name to retrieve the room number.

5. **Update Reservations**:
   - Choose option `4` and provide the reservation ID to update the guest name, room number, or contact number.

6. **Delete Reservations**:
   - Choose option `5` and provide the reservation ID to delete a reservation.

7. **Exit**:
   - Choose option `0` to exit the system.

---

## Code Structure

- **`HotelManagementSystem.java`**: The main class containing the program logic and database operations.
- **Database Operations**:
  - `reserveRoom()`: Adds a new reservation.
  - `viewReservations()`: Displays all reservations.
  - `getRoomNumber()`: Retrieves the room number for a reservation.
  - `updateReservation()`: Updates an existing reservation.
  - `deleteReservation()`: Deletes a reservation.
  - `reservationExists()`: Checks if a reservation exists.

---

## Screenshots

![Main Menu](screenshots/main_menu.png)  
*Main Menu of the Hotel Management System*

![View Reservations](screenshots/view_reservations.png)  
*Viewing Reservations in Table Format*

---

## Contributing

Contributions are welcome! If you find any issues or want to enhance the project, feel free to open a pull request.

---

## Acknowledgments

- Thanks to MySQL for providing the JDBC driver.
- Inspired by simple Java-based management systems.

---
