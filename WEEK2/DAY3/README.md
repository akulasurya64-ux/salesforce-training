# Salesforce Summer Program – Day 10 Mini Project

## Project Name
College Management System

## Project Overview
This project is a mini enterprise-level Salesforce application developed using multiple Salesforce technologies integrated together into one connected system.

The application manages:
- Students
- Faculty
- Courses
- Departments
- Course Registration
- Attendance Monitoring

The project demonstrates how frontend, backend, automation, database, and event-driven architecture work together in real Salesforce applications.

---

# Technologies Used

- Salesforce CRM
- Lightning Web Components (LWC)
- Apex
- SOQL
- Validation Rules
- Flow Automation
- Formula Fields
- Triggers
- Salesforce Objects & Relationships

---

# CRM Concepts

## Main CRM Entities
### Student
Stores:
- Name
- Email
- Department
- Attendance
- Registered Courses

### Faculty
Stores:
- Faculty Name
- Assigned Courses
- Department

### Course
Stores:
- Course Name
- Capacity
- Remaining Seats

### Department
Stores:
- Department Name
- Faculty List
- Student List

---

# Data Model

## Objects Created
### Custom Objects
- Student__c
- Faculty__c
- Course__c
- Department__c
- Registration__c

## Relationships
- Student → Department (Lookup)
- Faculty → Department (Lookup)
- Course → Faculty (Lookup)
- Registration → Student (Master-Detail)
- Registration → Course (Master-Detail)

---

# Validation Rules

## Rules Implemented

### Email Validation
- Student email cannot be blank.

### Course Seat Validation
- Students cannot register if seats exceed the limit.

### Attendance Validation
- Attendance percentage cannot exceed 100%.

---

# Formula Fields

## Remaining Seats
Calculates:
Available Seats = Total Seats - Registered Students

## Attendance Percentage
Automatically calculates student attendance percentage.

---

# Flow Automation

## Auto Confirmation Email
When a student registers:
- Flow sends confirmation email automatically.

## Attendance Warning
If attendance falls below threshold:
- Warning notification is generated.

---

# Apex Logic

## Eligibility Calculation
Checks whether:
- Student is eligible for registration
- Attendance requirements are satisfied

## Bulk Operations
Handles:
- Multiple student registrations efficiently
- Large-scale data updates

---

# SOQL Usage

Used to:
- Retrieve student records
- Fetch course details
- Display faculty assignments
- Load dashboard data

Example:
```sql
SELECT Name, Email__c FROM Student__c
