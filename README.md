# Ticketing UI
## Files Included
### [index.html](index.html)
The main homepage. It displays a title "Nowtrack", inspired by the name of USA's train system, Amtrack.
- Four buttons are displayed:
  - Book : opens [book.html](book.html)
  - My Trip : opens [ticket.html](ticket.html)
  - My Account : blank button to fill space, later implementation.
  - Customer Service : blank button to fill space, to maybe later implementation.

### [book.html](book.html)
Displays user input options for booking their ticket. 
- Some Features:
  - Takes in three user inputs (Travel Date, Number of Travelers, and Destination).
  - Travel Date requires month input before day input to properly display the right amount of days in the month.
    - this code was helped by ChatGPT.
  - writeCSVFile() is called and creates reservations.csv (to be replaced)
      - possible database to hold this information can be implemented at a later time.
    - Booking Number is displayed to show everything worked correctly.
    - User is presented with "Home" and "See Ticket" buttons.
   
### [ticket.html](ticket.html)

## Code and Features Explained
### [book.html](book.html)
Displays user input options for booking their ticket. 
- There is an if statement that checks if all input values have been properly filled.
  - It will give an alert to tell the user to input all values if this if statement isn't statisfied. 
- writeCSVFile() creates a .csv file to hold booking information.
  - calls generateReservationNumber() to create a reservation number between 0001 - 9999
  - formats date from 2024 [Month] [Day] --> 2024-MM-DD
 
### [ticket.html](ticket.html)
The following instructions are how to use this page:
1. Click "Load Booking Data" (it is preconfigured to load a file named "reservations.csv" 
2. Type in your reservation number (it must be 4 digits)
3. Press "Confirm"
4. The details of your reservation will show!

- Within ticket.html, it has a functions loadCSV() and parseCSV() that parces through the file to store it locally while the file is running in the browser.
- the function getTicket() pulls data from the array that was created with parseCSV() to find the booking details according to the provided reservation number. 
