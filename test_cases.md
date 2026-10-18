# test_cases.md --  Simulated Device Monitoring and Alert System

Tested by: Jeziel Alfon Siscon  
Date: October 18, 2026  

| Test Case | Input or Action | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|---|
| TC01 | Choose 1 | Five readings displayed: 28, 31, 35, 37, 29 | Five readings displayed correctly | Pass |
| TC02 | Choose 2, enter 33 | "Reading added successfully." | "Reading added successfully." | Pass |
| TC03 | Choose 2, enter abc | Rejected; list unchanged | Rejected; enter a whole number only. | Pass |
| TC04 | Choose 2, enter -5 | Rejected; list unchanged | Rejected; enter a value from 0 to 100. | Pass |
| TC05 | Choose 2, enter 120 | Rejected; list unchanged | Rejected; enter a value from 0 to 100. | Pass |
| TC06 | Add 30, then choose 3 | 30°C classified as WARNING | 30°C -> WARNING | Pass |
| TC07 | Choose 3 | 35°C classified as WARNING | 35°C -> WARNING | Pass |
| TC08 | Choose 4 (initial data) | Total 160, Avg 32.00, Min 28, Max 37, Status ATTENTION REQUIRED | Total 160, Avg 32.00, Min 28, Max 37, Status ATTENTION REQUIRED | Pass |
| TC09 | Enter 9 | Error message; menu shown again | Invalid choice message; menu redisplayed | Pass |
| TC10 | Choose 5 | Exit message; program ends | Thank you message; program terminated | Pass |

## Bugs Found and Fixed
- During initial testing of boundary condition evaluation (30 and 35), value comparisons initially used strict inequalities (< instead of <=), which incorrectly classified 30 as "NORMAL" and 35 as "NORMAL" or "CRITICAL". This was resolved by updating "classify_reading()" to include inclusive comparison operators (<= 35), ensuring that both 30°C and 35°C correctly evaluate to "WARNING".