***Bluetooth Attendance Server***

This repository contains the server-side component of the Bluetooth Attendance Checker system, designed to track student attendance in university lecture halls using Bluetooth Low Energy (BLE). The system is designed to prevent fraudulent attendance by ensuring students must be physically present to be marked as attending.

***Overview***

The Bluetooth Attendance Server is implemented using a Raspberry Pi that acts as a central scanner for BLE advertisements broadcast by student devices running the companion Bluetooth Attendance Checker app. The server collects student numbers, verifies attendance, and integrates with university systems for record-keeping.

***Features***

BLE-Based Attendance Verification: Detects students' smartphones via BLE to verify attendance.

Secure Authentication: Works alongside a mobile application where students log in to their university accounts.

Integration with AWS & Blackboard:
Uses AWS EC2 instances to host a Blackboard Learn developer environment.
The attendance data can be uploaded to Blackboard, allowing automated attendance tracking for university courses.

***Integration with Blackboard and AWS***

This system leverages Amazon Web Services (AWS) to deploy an instance of Blackboard Learn, allowing seamless integration with university learning management systems. The server:

Captures student attendance data from BLE broadcasts.

Attempts to update Blackboard’s Attendance API to reflect student presence.

Falls back to storing attendance logs for manual upload if API access is restricted.


