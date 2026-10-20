# Refactoring Report — Task 2

## Overview

The Student Register CLI from Task 1 was refactored into an object-oriented design. The application's existing features and console behavior were preserved.

## What Got Easier

1. **Data management:** The `Student` class encapsulates student data and provides controlled access through getters and setters.
2. **Maintenance:** The `StudentService` class contains the add, list, search, delete, and summary operations. Business logic is no longer mixed with the menu loop.
3. **Testing and reuse:** Service operations can be tested independently of console input and output, making future maintenance easier.

## What Got Harder

The initial refactoring required additional files and coordination between classes. Operations that previously accessed strings directly now work with `Student` objects and their methods.

## Classes and Responsibilities

- `Student`: Represents a student and encapsulates the student's name.
- `StudentService`: Manages the student collection and implements the five register operations.
- `Main`: Displays the menu, accepts user input, and calls the service.

## Behavior Verification

The application was manually tested after refactoring.

- Adding records: Passed
- Listing records: Passed
- Searching records: Passed
- Deleting records: Passed
- Displaying the summary: Passed
- Exiting the application: Passed

The application continues to use in-memory storage. Records are cleared when the program exits.

## Conclusion

The refactoring improved separation of responsibilities and encapsulation without adding new application features.