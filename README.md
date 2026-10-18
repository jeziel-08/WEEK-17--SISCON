# Simulated Device Monitoring and Alert System

Student Name: Jeziel Alfon Siscon  
Student Number: 2601317 
Section: 1CpE-B  

## Project Description
This program monitors simulated device-temperature readings for a Computer Engineering laboratory environment. It stores temperature data, allows users to append validated new readings, classifies each value into categories (NORMAL, WARNING, CRITICAL), and calculates detailed numerical summaries including overall system status.

## Features
- View all stored temperature readings with indexed position numbers.
- Add new readings with strict input validation (accepts whole numbers from 0 to 100 only).
- Classify every temperature reading based on predefined boundary rules.
- Generate a full statistical summary including total, average, minimum, maximum, category counts, percentages, and overall device status.
- Handle invalid menu selections and erroneous data inputs robustly without crashing.

## Requirements
- Python 3  (no external packages)

## How to Run
1. Open a terminal inside the Week17 folder.
2. Run the program using the command:
   python device_monitor.py

     
## Sample Output 

SIMULATED DEVICE MONITORING SYSTEM
[1] View Readings
[2] Add Reading
[3] Classify Readings
[4] Generate Summary
[5] Exit
Enter choice: 1

CURRENT READINGS
Reading 1: 28°C
Reading 2: 31°C
Reading 3: 35°C
Reading 4: 37°C
Reading 5: 29°C

 
## Test Cases 
I performed 10 tests. 10 passed and 0 failed.
Full details are in test_cases.md.

  
## Known Limitations
- Readings are lost when the program closes.
- Supports whole numbers (integers) only; decimal inputs are treated as invalid format errors.

## Reflection
Sometimes I wonder why I chose Computer Engineering because it is genuinely hard. I hope I can stay here in BS CpE, learn a lot, and build stronger skills in coding. It’s been one semester, and even though this is finals week, I still find it tough to catch up. I listen during lectures, but college requires a lot of self-learning, and with so many programming topics, it is easy to forget things along the way. I really hope to improve, understand everything by heart, and eventually handle future projects entirely on my own without needing help. Even with these struggles, working on this project really helped me see how all the programming blocks we learned throughout the semester finally connect. But i still did my best to do this work.


Almost everything about this project felt hard. As a first-year student trying to catch up during finals week, dealing with strict input validation, manual loops, and boundary checks all at once felt overwhelming. A specific bug I encountered was with the boundary conditions, where temperature limits like 35°C were incorrectly classified until I fixed the comparison operators to be inclusive. Despite how tough it was, working through it step-by-step by lookig at the lesson module given actually helped me see how all the programming blocks we learned throughout the semester fit together. For future improvements, I hope to practice more so I can build skills to code completely on my own without needing help.