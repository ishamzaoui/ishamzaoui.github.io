---
layout: post
title: "Hardware SMS API with SIM800L and Flask"
date: 2025-01-15 12:00:00 +0000
categories: projects hardware
tags: [SIM800L, Flask, API, UART, SQLite3, Logging, Hardware]
---

## Overview
This project is a **hardware-based SMS API** using the **SIM800L GSM module** for sending SMS and a **Flask REST API** for managing authentication, API keys, and logging. Key features include:

- **SIM800L module** for SMS transmission
- **UART communication** between SIM800L and a microcontroller/PC
- **Flask API with authentication**
- **SQLite3 database** for user and API key storage
- **Logging system** to track API requests
- **Error handling for hardware troubleshooting**
- **Admin dashboard** to manage API keys and apps

## Hardware Setup

### Components Used
- **SIM800L GSM Module**
- **ESP32/Raspberry Pi for UART communication**
- **CP2102 USB-to-TTL adapter**
- **Power supply (3.7V Li-ion or 5V with a step-down to 4.2V)**
- **Antenna for better GSM signal reception**

### Wiring Diagram
![SIM800L Wiring](https://ishamzaoui.github.io/images/projects/sms-api/home.png)

## Software Implementation

### Flask API
The Flask-based backend provides endpoints for:

- `/login` - User authentication
- `/dashboard` - App management UI
- `/api/sendsms` - Sends SMS using an API key
- `/apps/create` - Generates new API keys for apps

### SQLite3 Database
Stores:
- **Users** (with hashed passwords)
- **Apps** (each assigned a unique API key)
- **API logs** (to monitor requests and errors)

## Web Interface

### Login Page
![Login Page](https://ishamzaoui.github.io/images/projects/sms-api/img1.jpg)

### Dashboard
- View a list of API apps
- Generate new API keys
- Access API documentation

![Dashboard](https://ishamzaoui.github.io/images/projects/sms-api/img2.jpg)

### API Documentation
![API Documentation](https://ishamzaoui.github.io/images/projects/sms-api/img3.jpg)

## Hardware Troubleshooting
The system logs **SIM800L errors** and provides details on possible causes:
- `+CME ERROR: SIM not inserted` - Ensure the SIM card is properly seated and not locked by a PIN.
- `+CME ERROR: No network service` - Check the antenna connection, signal strength, and network coverage.
- `+CMS ERROR: Message failed` - Verify the recipient's phone number, available SMS credits, and proper UART configuration.

## API Usage
The `/api/sendsms` endpoint requires an API key and a JSON request:

```json
{
  "api_key": "your_api_key",
  "phone": "+1234567890",
  "message": "Hello, this is a test SMS!"
}
```

Response:
```json
{
  "status": "success",
  "message": "SMS sent successfully"
}
```

## Conclusion
This project offers a **secure and scalable** SMS solution by integrating **Flask, SQLite3, and SIM800L** with **error logging** and **API key management**. Future improvements may include **Twilio integration**, **multi-user support**, and **better error diagnostics**.

## Author
**HAMZAOUI**
---
