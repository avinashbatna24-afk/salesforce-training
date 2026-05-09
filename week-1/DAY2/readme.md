# Day 2 - Salesforce Platform Basics

## 1. What is Salesforce Platform?

Salesforce Platform is a cloud-based CRM platform that helps businesses manage customers, sales, services, and business operations in one place.

It provides:
- Data storage using Objects
- User interface using Apps and Tabs
- Automation tools
- Security and user management
- Development tools for customization

Salesforce uses multi-tenant architecture, where multiple companies use the same infrastructure while keeping their data secure and separate.

---

# Task 1: Connect Day 1 + Day 2

## How CRM Concepts Fit into Salesforce Platform

CRM concepts like:
- Account
- Contact
- Opportunity

are represented as Objects in Salesforce.

### Example

| CRM Concept | Salesforce Representation |
|---|---|
| Account | Object |
| Contact | Object |
| Opportunity | Object |

These objects are grouped inside an App such as the Sales App.

Users interact with them using Tabs.

### Flow

Customer Data → Stored in Objects → Accessed through Tabs → Organized inside Apps

---

# Task 2: Platform Understanding

## What is an App in Salesforce?

An App is a collection of related tools, tabs, objects, and features designed for a specific business purpose.

### Example

Sales App contains:
- Accounts
- Contacts
- Opportunities
- Reports

Apps help users work efficiently by organizing everything in one place.

---

## What is an Object?

An Object is like a database table used to store information in Salesforce.

Each object contains:
- Records
- Fields

### Example

Contact Object stores:
- Name
- Email
- Phone Number

### Types of Objects

1. Standard Objects  
   Examples:
   - Account
   - Contact
   - Opportunity

2. Custom Objects  
   Objects created according to business needs.

---

## What is a Tab?

A Tab is a user interface element used to open and access objects, dashboards, reports, or webpages.

### Example

- Contact Tab → Opens Contact records
- Opportunity Tab → Opens Opportunity records

Tabs help users navigate through Salesforce easily.

---

# Difference Between App and Object

| App | Object |
|---|---|
| Collection of tools and features | Stores data |
| Used for navigation and workflow | Used for managing records |
| Contains tabs and objects | Contains fields and records |
| Example: Sales App | Example: Contact Object |

---

# Task 3: Configuration vs Coding

## Configuration (No Code)

Configuration means customizing Salesforce using clicks and built-in tools without programming.

### When to Use

- Simple business automation
- Validation rules
- Workflow setup
- Form customization

### Examples

1. Creating a custom object for Student Records  
2. Creating validation rules for phone numbers

---

## Coding (Apex)

Coding is used when requirements are complex and cannot be solved using configuration alone.

Salesforce uses Apex programming language for development.

### When to Use

- Complex automation
- API integrations
- Advanced business logic
- Custom functionality

### Examples

1. Sending automatic emails based on complex conditions  
2. Integrating Salesforce with a hospital management system

---

# Task 4: Real System Thinking

## Example System: College Management System

### App Name

College Management App

---

## Objects Inside the App

| Object Name | Purpose |
|---|---|
| Student | Store student details |
| Faculty | Store faculty details |
| Course | Store course information |
| Attendance | Track attendance |
| Examination | Store exam results |

---

## How Users Will Interact

### Students
- View attendance
- Check marks
- View course details

### Faculty
- Update attendance
- Upload marks
- Manage courses

### Admin
- Manage students and faculty
- Generate reports
- Monitor system activities

---

# Multi-Tenant Architecture

Multi-tenant architecture means multiple organizations use the same Salesforce infrastructure while keeping their data private and secure.

### Benefits

- Lower cost
- Automatic updates
- Scalability
- Better maintenance

---

# How Salesforce Allows Developers to Extend Functionality

Salesforce allows developers to extend functionality using:
- Apex
- Lightning Components
- APIs
- Triggers
- Custom Objects
- Visualforce Pages

This helps businesses build customized applications according to their requirements.

---

# Answers for Evaluation Questions

## 1. What is an App in Salesforce?

An App is a collection of related tabs, objects, and tools designed for a specific business process.

---

## 2. What is an Object?

An Object is a database table used to store data in Salesforce.

---

## 3. Difference between App and Object

An App organizes features and navigation, while an Object stores data records.

---

## 4. What is Multi-Tenant Architecture?

It is an architecture where multiple organizations share the same Salesforce infrastructure while keeping their data secure and isolated.

---

## 5. When should we use configuration instead of code?

Configuration should be used when requirements can be solved using built-in tools without complex programming.

---

## 6. How does Salesforce allow developers to extend functionality?

Salesforce provides Apex, APIs, Lightning Components, and custom development tools to extend platform functionality.

---

# Screenshots



