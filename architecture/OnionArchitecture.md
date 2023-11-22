# Onion Architecture
Onion architecture is a way of structuring an API to have separation of concerns.

There are for segments to the onion including:
- API
- Application
- Domain
- Infrastructure

# API
The API layer is concerned about the the objects coming and going from the application and the controller definitions.

# Application
The Application layer is where the business logic is applied.

# Domain
Domain contains the business logic object definitions for the API. These can be the same as the DTOs in the controllers, or they can be different. They can be the same as the tables in the database or they can be different. In any case you should be taking the values from the DB tables and the DTOs and transforming them into a format that fits the business logic of the application.

# Infrastructure
This project will setup integrations with other services and the foundation for the API.
