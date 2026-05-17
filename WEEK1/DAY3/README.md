##Differences between App,Object,Record and Field

Term	Definition	Real-Life Example
App	Collection of related tools, tabs and objects	College Management App
Object	Database table storing similar data	Student Object
Record	Single entry inside an object	One student’s details
Field	Individual piece of information	Student Name
Detailed Explanation
App

An app is a collection of related functionalities used together for a business process.

Example

A College Management App may contain:

Student Object
Faculty Object
Course Object
Department Object

Apps help users access related data from one place.

Object

Objects are similar to database tables.

They store data related to a specific topic.

Example Objects
Student
Faculty
Course
Department

Each object contains multiple records.

Record

A record is a single row of data inside an object.

Example

Student Record:

Name: Rahul
Age: 20
Course: B.Tech

Every student will have a separate record.

Field

Fields store specific information about records.

Examples
Student Name
Email
Mobile Number
Department Name
Types of Fields
Field Type	Purpose
Text	Stores text values
Number	Stores numeric values
Date	Stores dates
Checkbox	Stores true/false values
Formula	Automatically calculates values

## Standard vs Custom Objects
Standard Objects

Standard objects are already provided by Salesforce.

These are commonly used in business applications.

Examples
Account
Contact
Opportunity
Lead
Custom Objects

Custom objects are created by users based on business requirements.

Examples in This Project
Student
Faculty
Course
Department

Difference Between Standard and Custom Objects

Standard Objects	Custom Objects
Created by Salesforce	Created by users
Predefined structure	Fully customizable
Used for common business needs	Used for organization-specific needs

## College Management System Data Model

Objects Created
1. Student

Stores student information.

Fields
Student ID
Name
Age
Email
Percentage
2. Faculty

Stores faculty details.

Fields
Faculty ID
Faculty Name
Subject
Email
3. Course

Stores course information.

Fields
Course Name
Total Seats
Enrolled Students
Remaining Seats
4. Department

Stores department information.

Fields
Department Name
HOD Name
Department Code
6. Relationships in Salesforce

Relationships are used to connect objects together.

Relationships help:

Link related data
Avoid duplicate information
Improve reporting
Maintain data consistency
Types of Relationships
Lookup Relationship
Master-Detail Relationship
Many-to-Many Relationship
7. Lookup Relationships

A lookup relationship creates a connection between two objects.

Objects remain independent even after linking.

Lookup Relationships Used
Parent Object	Child Object	Relationship Type
Department	Faculty	Lookup
Department	Course	Lookup
Course	Student	Lookup
Faculty	Course	Lookup
Relationship Explanation
Department → Faculty

One department can have many faculty members.

Example:

CSE Department
Faculty 1
Faculty 2
Faculty 3
Department → Course

One department can offer multiple courses.

Example:

CSE Department
Java
Python
DBMS
Course → Student

Many students can enroll in one course.

Example:

Java Course
Student A
Student B
Student C
Faculty → Course

One faculty member can teach multiple courses.

Data Model Diagram
Department
   |
   |---- Faculty
   |
   |---- Course
              |
              |---- Student
              
##Formula Fields

Formula fields automatically calculate values based on other fields.

Advantages of Formula Fields
Reduces manual work
Improves accuracy
Saves time
Provides real-time calculations
Formula Field Examples
1. Full Name Formula
First_Name + " " + Last_Name
Purpose

Automatically combines first and last names.

Benefit

Avoids repetitive typing.

2. Remaining Seats Formula
Total_Seats - Enrolled_Students
Purpose

Calculates available seats automatically.

Benefit

Prevents overbooking.

3. Percentage Formula
(Obtained_Marks / Total_Marks) * 100
Purpose

Calculates student percentage.

Benefit

Improves calculation accuracy.

Formula Fields vs Manual Calculations
Manual Calculation	Formula Field
Time-consuming	Automatic
Error-prone	Accurate
Needs repeated work	Updates automatically

## Validation Rules

Validation rules prevent incorrect or invalid data from being saved.

Why Validation Rules are Important

Validation rules help:

Maintain data quality
Prevent mistakes
Improve reliability
Ensure consistency
Validation Rule Examples
1. Email Cannot Be Empty
Rule

Student email must not be blank.

Problem Prevented

Prevents incomplete records.

2. Student Age Cannot Be Negative
Rule

Age must be greater than zero.

Problem Prevented

Stops invalid age entries.

3. Course Seats Cannot Exceed Limit
Rule

Enrolled students must not exceed total seats.

Problem Prevented

Avoids over-allocation.

##Formula Fields vs Validation Rules

Formula Fields	Validation Rules
Calculate values	Restrict invalid data
Used for automation	Used for data quality
Example: Percentage	Example: Age validation
11. Importance of Structured Enterprise Data

Large organizations manage huge amounts of data every day.

Without proper structure:

Duplicate data increases
Errors occur frequently
Reports become inaccurate
Searching becomes difficult

Structured enterprise systems solve these problems.

Why Companies Cannot Depend Only on Excel Sheets

Excel sheets:

Become difficult to manage at scale
Cause duplicate entries
Lack strong relationships
Have limited automation
Create security risks

Salesforce solves these problems using structured objects and relationships.
