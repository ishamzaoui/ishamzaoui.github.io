---
layout: post
title: "Securinets TEK-UP Desktop Application"
date: 2024-10-27 12:00:00 +0000
categories: projects desktop-application
tags: [rfid, desktop application, .NET, sqlite3]
---

## Description
**Securinets TEK-UP** is a desktop application developed in **.NET VB** that connects to an RFID USB reader to capture data from RFID cards. It saves the presence information in an **SQLite3 database** for secure record-keeping. The app is designed to automate the process of attendance and presence tracking using RFID technology.

---

## Features
- **RFID Integration**: The app reads RFID cards connected via a USB reader.
- **SQLite3 Database**: All attendance data is saved in a lightweight SQLite3 database.
- **Real-time Tracking**: As soon as an RFID card is scanned, the presence data is saved in real-time.
- **User Management**: Add, edit, or delete users from the database.
- **Search Functionality**: Quickly search for users by ID, name, or surname.
- **Audio Feedback**: Play sounds and use text-to-speech for user feedback.
- **Excel Integration**: Store and manage data in an Excel file for easy access and reporting.

---

## Workflow

1. **RFID Card Scanning**:
   When an RFID card is scanned using the USB reader, the application reads the card's unique identifier.

2. **Database Insertion**:
   The application inserts the unique card identifier and timestamp into an SQLite3 database.

3. **View Attendance**:
   The saved presence data can be accessed and reviewed via the application interface.

---

## Application Interface

The user-friendly interface of **Securinets TEK-UP** allows seamless interaction. Users can view logs of card scans, check the current status of cards, and manage database records easily.

---

## Application Image
![Securinets TEK-UP Application Interface](https://ishamzaoui.github.io/images/projects/app.png)

---

## ID Card Image
![RFID Card](https://ishamzaoui.github.io/images/projects/card.png)

---

## Additional Functionalities
- **New User Registration**: Automatically detect new RFID cards and prompt for user registration.
- **Edit User Details**: Update user information such as name, surname, and access count.
- **Delete Users**: Remove users from the database if needed.
- **Real-time Data Loading**: Use a background worker to load data without freezing the UI.
- **Keyboard Input Handling**: Capture RFID card data via keyboard input for compatibility with various RFID readers.
- **Customizable Settings**: Enable or disable sounds, text-to-speech, and grid lines in the interface.

---

## Conclusion
**Securinets TEK-UP** is a reliable and efficient tool for automating attendance tracking with RFID technology. Whether for workplace security or educational purposes, the app makes it easy to monitor and store presence data securely.

---

## Author
**HAMZAOUI**

This application demonstrates the power of RFID integration with desktop applications in **.NET VB**, along with the simplicity and effectiveness of using **SQLite3** as a database solution.