# CarBookingSystem
Car Booking System
The Car Booking System is a Java-based application that allows users to rent and return cars seamlessly. It manages car availability, rental pricing, customer details, and provides a simple command-line interface for interaction.

Project Requirements & Functionalities

Requirements:
     A system to allow customers to book and return cars. 
     A mechanism to track available cars.
     Pricing calculation based on rental duration.
     A simple command-line interface for interaction.

Functionalities:

1.Car Management:
     Add new cars to the system.
     Track car availability.

2.Customer Management:
     Register customers when they rent a car.
     Store customer details for tracking rentals.

3.Booking System:
     Rent a car by selecting an available car and specifying rental duration.
     Generate a bill based on the rental period.
     Reduce the available car count after a successful booking.

4.Return System:
     Allow customers to return rented cars.
     Increase the available car count after return.

5.Display Available Cars:
     List all available cars with details.

6.Exit System:
     Close the application safely.


Technologies & Concepts Used

Programming Language: Java

Data Structures:
     Lists for managing cars, customers, and bookings.

OOP Concepts:
     Encapsulation (getter/setter methods).
     Abstraction (separate classes for Car, Customer, Booking, and Rental Service).

Exception Handling:
     Ensuring car availability before booking.

User Input Handling:
     Scanner class for command-line interactions.


Project Structure & Explanation
Package: com.jts.crs
Classes & Their Responsibilities:
1.Car
     Attributes: carId, brand, model, pricePerDay, noOfAvailableCar.
     Methods:
            calculatePrice(int days): Calculates the rental cost based on days.
            Getters and Setters for attributes.

2.Customer
     Attributes: id, name.
     Methods:
            Getters and Setters for attributes.

3.CarRentalService
     Attributes:
            List<Car> for storing car details.
            List<Customer> for tracking customers.
            List<BookedCarInformation> for active bookings.
     Methods:
            bookedCar(Car car, Customer customer, int days): Books a car if available.
            returnCar(Car car, BookedCarInformation bookedCarInformation): Handles car returns.
            addCars(Car car): Adds new cars.
            addCustomer(Customer customer): Registers a new customer.
            options(): Provides a user interface to interact with the system.

4.CRSEntry (Main Class)
     Initializes cars and the rental system.
     Calls options() to start the system.


Summary:
     This Car Booking System is a simple Java-based project that enables customers to rent and return cars through a command-line interface. It utilizes OOP principles and basic data structures to maintain a list of cars, customers, and bookings. The system efficiently manages car availability and calculates rental charges, providing a seamless rental experience. It is structured into multiple classes for better organization and maintainability.
