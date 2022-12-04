# Geogo-Nodejs


Simple Ticket Booking System 
 
 
*Please read carefully*
 
This assignment is to test your problem-solving skills and code practices.
Using typescript is considered a big bonus.
Using any of the following node js frameworks is acceptable (ExpressJS, Fastify, NestJs , or AdonisJS).
Using a node.Js framework like Next.Js is acceptable.
Using any of the following databases is acceptable (MongoDB, PostgreSQL, or MySQL)
 
 
Description: Using this system normal users will be able to buy tickets for events. 
You have to create a Node.Js application, using which the admin users will be able to perform following actions (you have to create the following UI here in this app only):
Login to admin account
View all events
Create new event
Configure available tickets for an event for given dates.
Publish/unpublish events
See the list of reservations for an event.
The Node.Js app also needs to expose multiple API endpoints, using which you will be able to reserve event tickets for normal users.
You have to create a React.Js application for normal users, using which they will be able to perform following actions:
Create a new account
Login to account
View list of events
Reserve tickets for events
See the list of reserved events with details
Logout from account.
 Create the following data models in the DB using any ORM you see fitting (don’t use plain SQL queries).
 
User Model: containing the following data types -> _id, mobile number, email, password, full name, role (normal_user, admin_user).
Seed or auto-generate an admin user with any credentials you want, to manage events.
 
Event Model: containing the following data types -> _id,slug,  name, description, poster, start date, end date, published (only published events within the start_date and end_date range should be visible to normal users).
 
The admin user will be able to create, read, update and delete events.
 
Sample table:
 
_id                             
slug
name
description
start_date
end_date
published
1
avatar-2
Movie: Avatar 2
Avatar 2 by James Cameron
01-12-2022
31-12-2022
true
2
star-wars
Movie: Star Wars
Star Wars The Last Jedi
01-01-2023
31-01-2023
false

(you are free to do improvisations, if required)
 
Ticket: containing the following -> _id, event(foreign key to events table),  name, description, price and quantity.
 
Admin users can create multiple ticket slots for any event.
 
Sample table:
_id
event
date
description
price
total_quantity
available_quantity
1
1
01-12-2022
14:00-17:00
300
100
99
2
1
01-12-2022
17:30-20:30
450
100
100
3
1
02-12-2022
14:00-17:00
350
100
100

(you are free to do improvisations, if required)
 
 
Orders: containing the following -> _id, owner (user), event (foreign key to events table), ticket(foreign key to tickets table), purchase_date, total_price, status (confirmed, cancelled).
 
Normal logged-in users (from React.Js app) will be able to reserve tickets for a given event and that information needs to be kept in the orders table.
 
We need to create the following API endpoints in the Node.Js app, which the React.js app can use to build the frontend:
 
 
