# Hotel Reservation Demo

This application has front end developed using React.js and API service implemented using ballerina to demo simple hotel reservation usecase.

# How to Run 

1. Goto backend directory and then run `bal run`
2. Goto root directory and then run
   
   ```
   npm install
   npm start
   
   ```

3. Visit the `http://localhost:3000/reservations`


# How to Implemet Hotel Reservation API

## Prerequisites

* ballerina
* npm

## Steps

1) Clone Git Repo https://github.com/ballerina-guides/hotel-reservation-demo
2) Goto backend directory.
3) Refer `backend/README.md` and generate the Record types for the service.
4) Add a http service component implement API for hotel reservation front end. 
   It should provide following API paths. Refer README.md for more on service resources.

   1) Get available room types
   2) Create a reservation
   3) Update the reservation
   4) Get user reservations
   5) Delete the reservation

5) Improve tests add a reservatio with following reservation.

```
{
   checkinDate: "2024-02-19T14:00:00Z", 
   checkoutDate: "2024-02-20T10:00:00Z", 
   rate: 100, 
   user: user, 
   roomType: "Family"
}

```


## TIPS: 
   
1)  Use two tables for Rooms and Reservations.
   
   ```
   table<Room> key(number) rooms;

   table<Reservation> key(id) roomReservations = table [];
   
   ```
   
2)  Use utils functions in utils.bal file.
