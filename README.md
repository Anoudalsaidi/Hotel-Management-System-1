# Hotel Management System

## Overview

The Hotel Management System is a console-based application designed to manage hotel operations, including guest registration, room booking, check-in, check-out, and booking cancellations. The system helps hotel staff efficiently manage room availability and calculate the total cost of guest stays.

## Features

### Guest Management

* Register new guests.
* Store guest information and booking history.
* Manage guest check-in and check-out records.

### Room Management

* Add hotel rooms to the system.
* Support different room types:

  * Single
  * Double
  * Suite
* Assign a nightly rate for each room type.
* Track room availability status.

### Booking System

* Create room bookings for guests.
* Ensure a room can have only one active booking at a time.
* Store booking details including check-in and check-out dates.
* Prevent booking of unavailable rooms.

### Check-In Management

* Record guest check-ins.
* Create a check-in record when the guest arrives.
* Update room status to occupied.

### Check-Out Management

* Process guest check-outs.
* Calculate the total stay cost based on:

  * Number of nights
  * Room nightly rate
* Mark rooms as available after check-out.

### Booking Cancellation

* Allow guests to cancel bookings before check-in.
* Automatically free the reserved room.
* Update room availability immediately.

## System Entities

### Guest

* GuestID
* FullName
* Email
* PhoneNumber

### Room

* RoomID
* RoomNumber
* RoomType
* NightlyRate
* IsAvailable

### Booking

* BookingID
* BookingDate
* CheckInDate
* CheckOutDate
* Status
* GuestID
* RoomID

### CheckIn

* CheckInID
* CheckInDate
* GuestID
* BookingID

## Business Rules

1. A guest must be registered before making a booking.
2. A room can only have one active booking at a time.
3. Only available rooms can be booked.
4. A check-in record is created when the guest arrives.
5. The total stay cost is calculated using the number of nights multiplied by the room's nightly rate.
6. After check-out, the room becomes available for future bookings.
7. A booking can be cancelled only before check-in.
8. Cancelling a booking immediately makes the room available again.

## Expected Outputs

* List of registered guests.
* List of rooms and their availability status.
* Active bookings report.
* Check-in records.
* Check-out summaries.
* Booking cancellation records.
* Total revenue and stay cost calculations.

## Technologies Used

* C#
* .NET
* Entity Framework Core
* SQL Server

## Project Goal

The goal of this project is to automate hotel room reservations, manage guest stays efficiently, track room availability, and provide accurate billing based on room rates and stay duration.
