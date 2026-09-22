# Employee Leave Management – Leave Request

## 📌 Project Overview

The **Employee Leave Management – Leave Request System** is a simple system designed to manage employee leave requests.

The system allows employees to create leave requests by entering the required leave details and leave dates. The request is then assigned to the respective manager, who can review, approve, or reject the request.

The system also maintains employee details, manager details, leave requests, leave dates, approval information, leave balance, and leave request history.

---

## 🎯 Problem Statement

Develop an **Employee Leave Request System** that allows employees to submit leave requests with the required leave details and dates.

The request is sent to the assigned manager for approval or rejection. After the manager's decision, the system updates the leave request status and notifies the employee.

---

## ✨ Features

The project consists of the following main features:

### 1. Employee Details

The system stores employee information such as:

- Employee ID
- Employee Name
- Department
- Designation
- Email / Contact

### 2. Manager Details

The system maintains manager information including:

- Manager ID
- Manager Name
- Department
- Manager Email

### 3. Leave Request

Employees can create a leave request containing:

- Leave Request ID
- Leave Type
- Reason for Leave
- Number of Leave Days
- Available Leave Balance

### 4. Leave Date

The system manages leave dates including:

- Leave Start Date
- Leave End Date
- Total Leave Days
- Date Validation
- Overlapping Leave Check

### 5. Approval

Managers can review submitted leave requests and:

- Approve the leave request
- Reject the leave request
- Add approval/rejection comments
- Update request status
- Notify the employee

---

## 🔄 Leave Request Workflow

The general workflow of the system is:

```text
Start
  ↓
Employee Login
  ↓
Enter Employee Details
  ↓
Enter Leave Request Details
  ↓
Enter Leave Start Date & End Date
  ↓
Validate Leave Details
  ↓
Are the details valid?
  ├── No → Show Error → Correct Details → Validate Again
  │
  └── Yes
        ↓
Check Leave Balance & Overlapping Leave
        ↓
Submit Leave Request
        ↓
Send Request to Manager
        ↓
Manager Reviews Request
        ↓
Approve or Reject?
   ┌────┴────┐
   ↓         ↓
Reject     Approve
   ↓         ↓
Enter      Update Status
Rejection  as Approved
Reason       ↓
   ↓       Update Leave
Update     Balance
Status       ↓
as Rejected Notify Employee
   ↓
Notify Employee
   ↓
  End

📊 Leave Request Status
Pending
   ↓
Manager Review
   ↓
 ┌───────────────┐
 ↓               ↓
Approved       Rejected

🏗️ System Components
Employee Details
       │
       ↓
Manager Details
       │
       ↓
Leave Request
       │
       ↓
Leave Date
       │
       ↓
Approval

🗂️ Project Structure
Employee-Leave-Management/
│
├── README.md
│
├── docs/
│   ├── ER-Diagram.png
│   ├── Flowchart.png
│   └── Algorithm.txt
│
├── src/
│   ├── employee/
│   ├── manager/
│   ├── leave-request/
│   └── approval/
│
└── database/
    └── schema.sql

🔄 Approval Process
Employee
   │
   │ Submit Leave Request
   ↓
Leave Request
   │
   │ Assigned to Manager
   ↓
Manager Review
   │
   ├───────────────┐
   ↓               ↓
Approve          Reject
   │               │
   ↓               ↓
Update Status    Enter Reason
   │               │
   ↓               ↓
Update Balance   Update Status
   │               │
   └───────┬───────┘
           ↓
    Notify Employee

📋 Example Leave Request
Leave Request ID : LR001
Employee ID      : EMP001
Leave Type       : Casual Leave
Reason           : Personal Work
Start Date       : 10-10-2026
End Date         : 12-10-2026
Total Leave Days : 3
Leave Balance    : 12
Status           : Pending
Manager ID       : MGR001

📄 License

### Recommended GitHub files

Since you already have the **ER diagram, flowchart, and algorithm** for this assignment, a clean repository could look like:

```text
Employee-Leave-Management/
│
├── README.md
├── docs/
│   ├── ER-Diagram.png
│   ├── Flowchart.png
│   └── Algorithm.txt
│
├── src/
└── database/
