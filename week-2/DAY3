## 1. App vs. Object vs. Record vs. Field

To understand how Salesforce structures data, it helps to think of it like a digital filing system:

* **App:** The filing cabinet. It is a workspace containing a set of tools, tabs, and objects tailored for a specific team or business process (e.g., a "Campus Connect" app for the admissions team).
* **Object:** A specific folder inside the cabinet, or a tab in a spreadsheet. It is a database table that stores a specific kind of entity (e.g., the `Student` object or `Course` object).
* **Record:** A single document inside the folder, or a single row in the spreadsheet. It represents one specific instance of an object (e.g., a record for "Thafil").
* **Field:** The specific fill-in-the-blank lines on that document, or the columns in a spreadsheet. It stores distinct pieces of information about the record (e.g., "First Name", "Email", "GPA").

---

## 2. Standard vs. Custom Objects

* **Standard Objects:** These are pre-built objects that come included with Salesforce right out of the box. Examples include `Account`, `Contact`, `Lead`, and `Opportunity`. They handle standard CRM (Customer Relationship Management) business logic.
* **Custom Objects:** These are objects created by the system administrator to store information unique to the organization's specific needs. In our college system, things like `Professor__c` or `Course__c` are custom objects (denoted by the `__c` suffix).

---

## 3. Your College Data Model

This model tracks how Students interact with Courses through a central Enrollment hub.

### Objects & Relationships
* **Department to Professor:** *Lookup Relationship* (One department has many professors).
* **Professor to Course:** *Lookup Relationship* (One professor teaches many courses).
* **Student to Course:** *Many-to-Many Relationship*. This is achieved using `Enrollment__c` as a **Junction Object** with Master-Detail relationships to both Student and Course.

### Data Model Diagrams

<table>
  <tr>
    <td width="50%">
      <b>Conceptual Data Model</b><br>
      <img src="Academic Department-2026-05-11-103115.png" alt="Conceptual Data Model Diagram">
    </td>
    <td width="50%">
      <b>Salesforce Schema Builder Execution</b><br>
      <img src="Screenshot 2026-05-11 155852.png" alt="Salesforce Schema Builder Screenshot">
    </td>
  </tr>
</table>

---

## 4. Formula Fields

**Explanation:** Formula fields are read-only fields that automatically calculate their value based on other fields, expressions, or values. They are dynamic, meaning if the underlying data changes, the formula output instantly updates.

**My Examples:**
* **`Full_Name__c` (Text):** Instead of manually typing the full name, this formula combines the first and last name fields. 
    * *Formula:* `First_Name__c & " " & Last_Name__c`
* **`Honor_Roll_Eligible__c` (Checkbox):** Automatically checks a box on the student's record if their CGPA meets the threshold.
    * *Formula:* `CGPA__c >= 3.5`

---

## 5. Validation Rules

**Explanation:** Validation rules verify that the data entered by a user meets specific organizational standards before the record can be saved. If the rule evaluates to "True" (meaning the error condition is met), Salesforce prevents the save and displays a custom error message.

**My Examples:**
* **`Prevent_Future_DOB`:** Prevents a user from accidentally setting a student's Date of Birth in the future.
    * *Error Condition:* `Date_of_Birth__c > TODAY()`
    * *Error Message:* "A student's Date of Birth cannot be in the future."
* **`Valid_GPA_Range`:** Ensures the GPA entered is a realistic number.
    * *Error Condition:* `CGPA__c < 0.0 || CGPA__c > 4.0`
    * *Error Message:* "Please enter a valid CGPA between 0.0 and 4.0."

---

## 6. Reflection: Why Structured Enterprise Data Matters

Structured enterprise data is the foundation of any scalable organization. Without a strict data model (objects, relationships, and validation rules), data becomes chaotic. Users might enter "Computer Science", "CS", or "Comp Sci" interchangeably, making reporting impossible. 

By enforcing structure, we create a "Single Source of Truth." It ensures data integrity, prevents duplicate or dirty data, and allows different departments (Admissions, Billing, Academics) to collaborate efficiently. Most importantly, structured data is what allows us to safely automate business processes, because the system can actually trust the data it is processing.
