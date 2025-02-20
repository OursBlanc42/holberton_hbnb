# HBNB PROJECT

## This document will regroup:

- Presentation of the HBnB project
- Presentation of the team
- Technical Document:
    - High-level package diagram
    - Detailed Class Diagram
    - Sequence diagram

---

## Presentation of the HBnB project

As students in development at Holberton School, we put into practice our knowledge in a project.
The project of the second trimester is to produce a clone of AirBnB called HBnB.

### What is AirBnB?

AirBnB is a service company that provides a platform to connect people who rent out part of their home with private individuals looking for accommodation.

### The key features of the AirBnB website are:

#### For people who rent:
- Create a page for their home and specify the location, amenities, price, availability dates, etc.

#### For people who want to rent:
- Select a place and date and view a list of available rentable homes.

Of course, there are many additional features derived from these two key concepts, which will be explained later in dedicated diagrams.

---

## The team is composed of:
- Ali MEDJNOUN 
- Warren NGOUABI 
- Simon REGNIER 

---

## High-Level Package Diagram

### Disclaimer
Due to some misunderstandings regarding this part of the project, we decided to provide a diagram that represents what we have understood about the architecture of the site, even though we acknowledge that it does not strictly follow the formal rules for producing a Package Diagram.

### Objective:
This diagram describes the architecture of the app (layered architecture).

### Overview:

#### Presentation Layer (Front-end):
- Manages interaction between clients and services through the API.

This layer contains the user interface and API

#### Business Layer (Back-end):
- Contains the core business logic of the application.

This layer works wwith User, Place, Review, and Amenity.
The data retrieve and store from the DB

#### Persistence Layer (Back-end):
- Manages data storage and retrieval.

This layer contains the DB.

[ package diagram ]

---

## Detailed Class Diagram

### Objective:
- Detail the "business layer."
- Define the architecture of this layer.
- Present the features of the app.

According to the specifications, we will use an OOP architecture and a Facade Pattern to centralize communication between the client and the business layer. 
The OOP architecture allows us to avoid code duplication by using a base model class and inheritance.

### Overview and Details:

#### Facade 
- Centralize communication between client and business layer.

#### BaseModel (abstract class)
- Provides a common base for all other objects.
- We added validation methods to ensure every input used in the app is properly validated.

#### User
- Stores user information.
- Open question regarding permissions management (admin access).
- Registrer is different from user creation, because only an admin can create a user from scratch, while regular customers must register their own accounts.
- The method for validating email is placed in `User` and not in the `BaseModel` because only the `user needs to validate an email.


#### Place
- Associates a place with an owner.
- Includes geographical and pricing attributes.

#### Amenity_entity
- Manages the available amenities that can be added to the amenity list of each place.

#### Review
- Manages 5-star reviews, including the author and the concerned place.

### Return of Methods:
- Boolean values (`True/False`) to indicate whether an action was successful or failed.

### Miscellaneous :
- Even if some methods in different classes seem similar, we prefer to distinguish them (one per class) because their constraints are not the same.
**Exemple**
A description, a comment, a password, and a name are all strings, but their length limits and specific constraints differ for each one.

[ class diagram ]

---

## Sequence diagram

to be completed

