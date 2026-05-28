# Day 10 Notes – Salesforce Summer Program

## Topic: Enterprise Application Integration Using Salesforce

---

# 1. Lightning Web Components (LWC)

## What is LWC?
Lightning Web Components is Salesforce’s modern UI framework used to build fast and reusable frontend components.

## Features
- Component-based architecture
- Reactive user interface
- Faster performance
- Reusable components
- Easy backend integration

## Important Concepts
- HTML template
- JavaScript controller
- Meta XML file
- Data binding
- Event handling

## Communication Types
### Parent to Child
Using `@api`

### Child to Parent
Using custom events

### Unrelated Components
Using pub-sub model

---

# 2. Salesforce Data Integration

LWC interacts with Salesforce backend using:
- Apex
- SOQL
- Wire service

## Purpose
- Retrieve records
- Update data
- Display dynamic UI

---

# 3. CRM Concepts

CRM = Customer Relationship Management

In this project:
- Students are managed
- Faculty information is stored
- Courses are tracked
- Departments are connected

---

# 4. Data Modeling

## Objects
Custom objects created:
- Student__c
- Faculty__c
- Course__c
- Department__c
- Registration__c

## Relationships
### Lookup Relationship
Loose connection between objects

### Master-Detail Relationship
Strong parent-child relationship

---

# 5. Validation Rules

Validation Rules ensure data integrity.

## Examples

### Email Validation
Student email cannot be blank.

### Seat Limit Validation
Students cannot register if course is full.

### Attendance Validation
Attendance percentage cannot exceed 100%.

---

# 6. Formula Fields

Formula fields automatically calculate values.

## Examples
### Remaining Seats
Remaining Seats = Total Seats - Registered Students

### Attendance Percentage
Automatically calculates attendance percentage.

---

# 7. Flow Automation

Flows automate repetitive business processes.

## Examples

### Registration Confirmation
Automatically sends email after registration.

### Attendance Alert
Warns students with low attendance.

## Advantages
- Reduces manual work
- Improves efficiency
- Saves time

---

# 8. Apex Programming

Apex is Salesforce backend programming language.

## Used For
- Complex business logic
- Bulk operations
- Custom automation
- Trigger handling

## Examples
- Eligibility checking
- Course registration logic

---

# 9. SOQL (Salesforce Object Query Language)

Used to fetch Salesforce records.

## Example Query

```sql
SELECT Name, Email__c FROM Student__c
