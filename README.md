# SalaryManagementSystem

It's a PL/SQL project. I created this project with distributed database.
Salary Management has 3 users

1. Admin/HR
2. Accountant
3. Employee

---

## Procedures and Functions

### **1. Admin Module**

#### **Procedures**

- **AddEmployee()**

  - **Usage:**
    > Add new employee and assign their salary
  - **Parameters:**
    > `Name`, `Gender`, `Email`, `JoiningDate`, `SID`
  - **Output:**
    > Add the person as employee and assign their salary

- **ChangeEmpPost()**
  - **Usage:**
    > Promote or demote employee
  - **Parameters:**
    > `EID`, `SID`
  - **Output:**
    > Changed pay scale with given Employee ID and SID

### **2. Accountant Module**

- **PaySalary()**
  - **Usage:**
    > Pay employees' salaries by calling the function `GenerateSalary()` and the procedure `TransectSalary()`
  - **Parameters:**
    > `EmployeeID`, `Month of Giving Salary`
  - **Output:**
    > Pay salary of the given Employee ID and month

#### **Procedures**

- **AddFund()**

  - **Usage:**
    > Increase fund
  - **Parameter:**
    > `Amount`
  - **Output:**
    > Increase fund with the given amount

- **AddLeave()**

  - **Usage:**
    > Add leaves for employees for a specific month
  - **Parameters:**
    > `EID`, `S_month`, `L_days`
  - **Output:**
    > Add leaves for the given Employee ID and month

- **TransectSalary()**

  - **Usage:**
    > Transaction procedure for payments; uses function `CheckValid()` and procedure `UpdateFund()` to complete
  - **Parameters:**
    > `EID`, `Amount`, `Month`
  - **Output:**
    > Transaction for payments

- **UpdateFund()**
  - **Usage:**
    > After transaction, the amount of payments will be reduced by this procedure
  - **Parameter:**
    > `Amount`
  - **Output:**
    > Updated fund after transaction

#### **Functions**

- **GenerateSalary()**

  - **Usage:**
    > Generate salary calculated with leaves of the given month
  - **Parameters:**
    > `EID`, `Month`
  - **Return:**
    > Generated salary

- **CheckValid()**
  - **Usage:**
    > Determines whether payment is payable or not
  - **Parameters:**
    > `EID`, `Month`
  - **Return:**
    > `1` for valid, `2` for invalid

### **3. Employee Module**

- **ViewDetails()**
  - **Usage:**
    > Show employee his/her details with payment history
  - **Parameter:**
    > `EmployeeID`
  - **Output:**
    > Show details of the given employee ID

---

> **Tip:**  
> Use these procedures and functions to manage employees, salary transactions, leaves, and administration efficiently.
