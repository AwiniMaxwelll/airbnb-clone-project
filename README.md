# airbnb-clone-project
                                       Project Overview

This is an Airbnb Clone Project, a full-stack web application designed to replicate the core functionality of a booking platform like Airbnb. The focus of this project is 
to build a scalable, secure, and efficient application using modern software development practices. 

                                      Project Goals
   •	Develop a robust booking platform with features like user authentication, property listings, and secure transactions.
   
   •	Master collaborative workflows using GitHub for version control and project management.
   
   •	Design a scalable relational database and secure APIs using Django and GraphQL.
   
   •	Implement automated CI/CD pipelines for efficient deployments.
   
   •	Document the project thoroughly to demonstrate planning and execution skills.

   
                                       Technology Stack
   •	Backend: Django (Python) for server-side logic and API development.
   
   •	Database: MySQL for relational data storage and management.
   
   •	API: GraphQL for flexible and efficient data querying.
   
   •	CI/CD: GitHub Actions and Docker for automated testing and deployment.
   
   •	Version Control: GitHub for repository management and collaboration.



                                    Team Roles
The Airbnb Clone Project is structured to be developed by people with distinct roles to ensure efficient collaboration and successful delivery. Below is a breakdown of each role and their responsibilities in the project:
    •	UI/UX Designer: Designs intuitive, user-friendly interfaces and craft seamless user journeys to enhance engagement and usability. Responsibilities included user res    earch, persona development, wireframing, prototyping, and creating visually appealing designs.

    •	Software Architect:  Will design the high-level software architecture, select the best tools for the project like (Django, MySQL, and GraphQL) and set code quality     standards. The architect ensures system stability and security through architectural decisions and code reviews.

    •	Backend Developer: Implements the core business logic, algorithms, and server-side functionality using Django. Responsibilities include building secure APIs with Gr    aphQL, integrating with MySQL, and ensuring scalable backend performance.

    •	Database Administrator (DBA): DBA is responsible for Designing and managing relational database using MYSQL, defining entities, attributes, and relationships. The 
    DBA will optimize database performance, ensuring data integrity, and maintaining secure data storage.

    •	DevOps Engineer: Facilitated collaboration between development and operations teams, building CI/CD pipelines using GitHub Actions and Docker. The DevOps engineer e    nsured fast, stable, and automated deployments while maintaining application stability.


                                Database Design

Entities and Fields
•	Users
    o	id: Unique identifier for each user (Primary Key).

    o	email: User’s email address for authentication and communication.

    o	password: Securely hashed password for user authentication.

    o	name: User’s full name for profile display.

    o	role: User role (e.g, guest, host) to determine permissions.

•	Properties
    o	id: Unique identifier for each property (Primary Key).
    o	title: Descriptive title of the property.
    o	description: Detailed description of the property’s features.
    o	location: Address of the property.
    o	price: Cost of renting the property.
•	Bookings
    o	id: Unique identifier for each booking (Primary Key).
    o	user_id: Reference to the user making the booking (Foreign Key).
    o	property_id: Reference to the booked property (Foreign Key).
    o	start_date: Start date of the booking.
    o	end_date: End date of the booking.
•	Reviews
    o	id: Unique identifier for each review (Primary Key).
    o	user_id: Reference to the user who wrote the review (Foreign Key).
    o	property_id: Reference to the reviewed property (Foreign Key).
    o	rating: Numerical rating of a property and services rended by a property owner to a customer.
    o	comment: Textual feedback about the stay.
•	Payments
    o	id: Unique identifier for each payment (Primary Key).
    o	booking_id: Reference to the associated booking (Foreign Key).
    o	amount: Total payment amount.
    o	payment_status: Status of the payment (e.g., pending, completed, failed).
    o	payment_date: Date and time the payment was processed.
Entity Relationships
    •	Users and Properties: A user can own multiple properties (as a host), and one user owns each property. This is a one-to-many relationship (one user to many 
    properties).
    •	Users and Bookings: A user can make multiple bookings (as a guest), and each booking is made by one user. This is a one-to-many relationship (one user to many 
    bookings).
    •	Properties and Bookings: A property can have multiple bookings, but each booking belongs to one property. This is a one-to-many relationship 
    (one property to many bookings).
    •	Properties and Reviews: A property can have multiple reviews, but each review is associated with one property. This is a one-to-many relationship 
    (one property to many reviews).
    •	Users and Reviews: A user can write multiple reviews, and each review is written by one user. This is a one-to-many relationship (one user to many reviews).
    •	Bookings and Payments: Each booking can have one payment, and each payment is associated with one booking. This is a one-to-one relationship 
    (one booking to one payment).

