# Hospital Management System

A simple, robust console-based Hospital Management System developed in C. The application provides basic management for hospital and patient records, with user authentication, colored interface, and multiple sorting, searching, and reporting features. Designed for learning, academic, or small-scale administrative usage.

---

## Features

- **User Authentication:**  
  - Sign-up and login system with secure password storage in `users.txt`
- **Hospital Management:**
  - Add new hospitals (ID, name, city, available beds, price per bed, ratings, reviews)
  - Display all hospital records in a table
  - Filter hospitals by city and sort alphabetically
  - Sort hospitals by bed price, available beds, hospital name, rating/reviews
- **Patient Management:**
  - Add and manage patient records (ID, name, age, disease, admitted hospital)
  - Display all patient records
  - Each patient record shows their admitted hospital’s name (resolved automatically)
- **Data Persistence:**  
  - All records are stored persistently in plain-text files (`hospitals.txt`, `patients.txt`, `users.txt`)
- **User Interface:**
  - Clean, menu-driven terminal interface
  - Rich console coloring for better readability (with ANSI color codes)
  - Clear prompts, validation, and input error handling

---

## Table of Contents

- [Features](#features)
- [Screenshots](#screenshots)
- [Installation](#installation)
- [Usage](#usage)
- [File Structure](#file-structure)
- [Technology Overview](#technology-overview)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## Screenshots

> _Add screenshots of the main menu, sample records, and colored output for better documentation._  
> E.g.  
> ![Main Menu Screenshot](screenshots/main_menu.png)

---

## Installation

1. **Clone the Repository**
    ```sh
    git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
    cd YOUR_REPO_NAME
    ```

2. **Compile the Code**
    - Windows:
      ```sh
      gcc -o hms.exe Hospital_Management_System.c
      ```
    - Linux/Mac (needs `conio.h` alternatives and color terminal):
      ```sh
      gcc -o hms Hospital_Management_System.c
      ```

    _Note: Developed and tested on Windows. For Linux/Mac, you may need to update/replace `conio.h` and clear-screen commands._

3. **Run:**
    ```
    ./hms.exe     # On Windows
    ./hms         # On Linux/Mac after suitable modifications
    ```

---

## Usage

1. **Start the program:**  
   The welcome banner and authentication menu appear.
   - Choose to sign up for a new account or log in if already registered.
   - After authentication, the main menu is displayed.

2. **Main Menu Options:**
   - **Hospital Management:**  
     - Add, view, or filter hospital records.
   - **Patient Management:**  
     - Add or view patients. Each patient is linked to a hospital by ID.
   - **Sorting:**  
     - Sort hospital records by price, available beds, name, or rating/reviews.
   - **Exit:**  
     - Saves all data automatically and closes the application.

3. **Data Files:**  
   - All entries are saved automatically, and you may view/edit them directly for inspection or backup.

---

## File Structure

```
Hospital_Management_System.c    # Main C source code
hospitals.txt                  # All hospital records (auto-created)
patients.txt                   # All patient records (auto-created)
users.txt                      # User credentials (auto-created)
screenshots/                   # (Optional) Screenshots for the README
README.md                      # This file
```

---

## Technology Overview

- **Programming Language:**  
  - C, compatible with C99 standard.
- **Design Paradigm:**  
  - Structured programming, data stored in flat text files.
- **Interface:**  
  - ANSI color codes for enhanced visual UI (works on most modern terminals).
  - Uses Windows-specific headers and commands (for `conio.h` and screen clear).

---

## Troubleshooting

- **Wrong/Empty screen or color:**  
  - On Linux/Mac, you may not see colors or get errors for `conio.h`. Remove/replace all code with `#include <conio.h>` and adapt clear screen/keyboard input code for your OS.
- **File/persistence bugs:**  
  - Ensure the application’s working directory has write permission.
- **Compilation errors:**  
  - Use GCC or similar C standard compilers. Ensure dependencies are available.
- **Data not saving:**  
  - All records are appended to text files in the current directory; if not, check for permission errors.
- **Username Exists:**  
  - Sign-up will not allow duplicate usernames.

---

## Contributing

- Fork the repository
- Create your feature branch (`git checkout -b my-feature`)
- Commit your changes (`git commit -am 'Add feature'`)
- Push to the branch (`git push origin my-feature`)
- Create a Pull Request  
  _All meaningful contributions are welcome!_

---

## License

This project is open source and licensed under the [MIT License](LICENSE).

---

## Acknowledgements

- Built by Muhammad Tahir Hussain, 2026.
- Thanks to the open source community for inspiration and support.
- Special thanks to ANSI/VT-color reference resources.

---

> _For academic, demonstration, and non-critical administrative use only._
