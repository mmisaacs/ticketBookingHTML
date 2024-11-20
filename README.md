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
  - When "Book" is pressed, it verifies if all user input options are filled.
  - writeCSVFile() is called.
    - a random reservation number between 0001 and 9999 is generated.
    - data is formatted for the csv file
    - reservations.csv file is created for users to overwrite current reservations.csv file within folder.
      - possible database to hold this information can be implemented at a later time.
    - Booking Number is displayed to show everything worked correctly.
    - User is presented with "Home" and "See Ticket" buttons. 
