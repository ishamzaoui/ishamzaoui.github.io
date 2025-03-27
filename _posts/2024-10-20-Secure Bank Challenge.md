---
layout: post
title: "Secure Bank Simulation Challenge"
date: 2024-10-20 00:00:00 +0000
categories: hardware-ctf-writeups
tags: [arduino, base64, security, challenge]
---

## Description
This challenge involves a simulation of a secure banking system using Arduino, hosted on [Wokwi](https://wokwi.com/projects/412259462761520129). Participants must interact with a keypad and LED system to unlock the flag. The flag is obfuscated through Base64 encoding and stored in reverse, adding layers of complexity.

## Objectives
- Decode the Base64-encoded PIN and flag.
- Reverse the flag to reconstruct the original string.
- Optionally, bypass the Arduino logic to retrieve the flag directly.

## Solution Workflow

### Step 1: Decode Base64 Strings
The system stores sensitive information, including the PIN and flag, in Base64 encoding. Using a Python script, these can be decoded into a human-readable format.

### Step 2: Reverse the Decoded Flag
Once decoded, the flag is stored in reverse order. Reversing it again retrieves the original flag.

### Step 3: Analyze and Modify Logic (Alternative)
By bypassing or altering Arduino logic, you can force the system to reveal the flag without meeting the original conditions.

## Python Script for Decoding
Here's a Python script to decode the Base64-encoded PIN and flag, as well as reverse the flag:

```python
import base64

def decode_and_reverse(base64_list):
    decoded_list = []
    for base64_string in base64_list:
        decoded = base64.b64decode(base64_string).decode('utf-8')
        reversed_decoded = decoded[::-1]
        decoded_list.append(reversed_decoded)
    return decoded_list

# Example Base64 values
pin_b64 = ["UElO"]  # Replace with the Base64 string for the PIN
target_flag_b64 = ["MTk2Mg=="]  # Replace with the Base64 string for the flag

# Decode the PIN
decoded_pin = [base64.b64decode(pin).decode('utf-8') for pin in pin_b64]

# Decode and reverse the flag
decoded_flag = decode_and_reverse(target_flag_b64)

print(f"Decoded PIN Array: {decoded_pin}")
print(f"Decoded and Reversed Flag Array: {decoded_flag}")
```

### Explanation of the Script:
1. **Base64 Decoding**: The `decode_and_reverse` function decodes the Base64-encoded strings and then reverses the decoded string to retrieve the original flag.
2. **PIN Decoding**: The PIN is decoded from Base64 directly without reversal.
3. **Flag Decoding**: The flag is decoded and reversed to get the original value.

## Arduino Logic Overview

### Input Validation:
- A numeric PIN is entered using a keypad.
- Correct PIN input initiates LED validation.

### LED States:
- Two LEDs must be in specific states to proceed.

### Flag Retrieval:
- If conditions are met, pressing # reveals the encoded and reversed flag.

### Obfuscation:
- Both the PIN and flag are stored in Base64 and reversed for added complexity.

## Alternate Solution

To bypass the challenge conditions:
1. Modify the Arduino code to ignore PIN and LED state validations.
2. Force the system to display the flag upon any interaction.

## Solve:
We can enter the encoded PIN '1962' and turn on the first and last LEDs to show the flag.

## Full Architecture
![Full Architecture](https://ishamzaoui.github.io/images/hardware/writeups/img1.jpg)

## Solve Output
![Solve Output](https://ishamzaoui.github.io/images/hardware/writeups/img2.jpg)

## Author
**HAMZAOUI**

This challenge highlights cryptographic concepts like Base64 encoding and basic embedded system security. It encourages participants to explore both reverse engineering and logical bypass techniques.
