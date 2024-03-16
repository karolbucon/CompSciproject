Description of the code:
Import necessary libraries: The datetime and json libraries are imported. datetime is used to handle dates (for due dates in transactions), and json is used to save and load data to and from a file.

Book Class: This class represents a book in the library. It has attributes like title, author, ISBN, and quantity. The display method is used to return a string representation of the book.

Patron Class: This class represents a library patron. It has attributes like name, ID, and contact. The display method is used to return a string representation of the patron.

Transaction Class: This class represents a transaction in the library (like checking out or returning a book). It has attributes like book, patron, due_date, and fine. The check_in and check_out methods are used to handle returning and borrowing books, respectively. If a book is returned after its due date, a fine is calculated at a rate of $1 per day late.

Library Class: This class represents the library itself. It has lists of books, patrons, and transactions. It has methods to add and remove books and patrons, search for a book by title, and manage transactions. The save_data and load_data methods are used to save and load the library’s data to and from a file.

Main Function: This function is the main entry point of the program. It creates a Library object and enters a loop where the user can choose to perform various actions like adding/removing books or patrons, searching for a book, managing transactions, or saving and exiting.

Code Structure:
Library Management System

- Book Class
   - title
   - author
   - ISBN
   - quantity
   - display()
   
- Patron Class
   - name
   - ID
   - contact
   - display()

- Transaction Class
   - book
   - patron
   - due_date
   - fine
   - check_in()
   - check_out()

- Library Class
   - books
   - patrons
   - transactions
   - remove_book()
   - add_patron()
   - remove_patron()
   - search_book()
   - manage_transaction()
   - save_data()
   - load_data()

- main()

Some Comments:
The Book class represents a book in the library. It has attributes like title, author, ISBN, and quantity. The display method is used to return a string representation of the book.
The Patron class represents a library patron. It has attributes like name, ID, and contact. The display method is used to return a string representation of the patron.
The Transaction class represents a transaction in the library (like checking out or returning a book). It has attributes like book, patron, due_date, and fine. The check_in and check_out methods are used to handle returning and borrowing books, respectively. If a book is returned after its due date, a fine is calculated at a rate of $1 per day late.
The Library class represents the library itself. It has lists of books, patrons, and transactions. It has methods to add and remove books and patrons, search for a book by title, and manage transactions. The save_data and load_data methods are used to save and load the library’s data to and from a file.
The main function is the main entry point of the program. It creates a Library object and enters a loop where the user can choose to perform various actions like adding/removing books or patrons, searching for a book, managing transactions, or saving and exiting.

Functionalities:
Start the Program: Run the Python script in your terminal or command prompt. This will start the program and load any saved data from the library.json file.
Main Menu: You will be presented with a menu of options:
1. Add book
2. Remove book
3. Add patron
4. Remove patron
5. Search book
6. Manage transaction
7. Save and exit

Add a Book: To add a book, select option 1. You will be prompted to enter the book’s title, author, ISBN, and quantity. The book will then be added to the library.
Remove a Book: To remove a book, select option 2. You will be prompted to enter the title of the book you want to remove. If the book is found in the library, it will be removed.
Add a Patron: To add a patron, select option 3. You will be prompted to enter the patron’s name, ID, and contact information. The patron will then be added to the library.
Remove a Patron: To remove a patron, select option 4. You will be prompted to enter the ID of the patron you want to remove. If the patron is found in the library, they will be removed.
Search for a Book: To search for a book, select option 5. You will be prompted to enter the title of the book you want to search for. If the book is found in the library, its details will be displayed.
Manage a Transaction: To manage a transaction, select option 6. You will be prompted to enter the title of the book and the ID of the patron involved in the transaction. A new transaction will then be created with a due date of 14 days from the current date.
Save and Exit: To save the library’s data and exit the program, select option 7. The library’s data will be saved to the library.json file, and the program will end.

Sample scenarios:
Adding a Book
book = Book("Harry Potter", "J.K. Rowling", "1234567890", 10)

library.add_book(book)

Checking out a Book

patron = Patron("John Doe", "001", "johndoe@example.com")

library.add_patron(patron)

transaction = Transaction(book, patron)

transaction.check_out()

Generating reports:

for book in library.books:
    print(book.display())

for patron in library.patrons:
    print(patron.display())

Findings thorughout the project:
Throughout the project I found that pyhtons object-oriented features make it easy to model real-world entities like books, patrons, and transactions. The use of classes and methods allows for a clear separation of concerns where each class is responsible for a specific part of the system.

Some Challenges faced:
The current implementation uses a simple file-based system (JSON) for data storage. This works for small libraries but might not scale well for larger libraries with thousands of books and patrons.
The code also does not have comprehensive error handling.
A graphical user interface (GUI) would provide a better user experience.

Improvements:
Develop a GUI using a web-based interface Django to make it easier to use.
Integrating a database system for data storage.
Add more features like books recommendations would provide a better service to the patrons.


