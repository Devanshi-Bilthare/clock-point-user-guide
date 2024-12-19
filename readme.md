# Clock Point User Guide

## Admin Credentials
**Email** : devanshi@gmail.com
**Password** : 123456

## Introduction
The **Clock Point Attendance Management System** is a robust web-based application designed to streamline attendance tracking, employee management, and salary processing for businesses. Built using the **MERN stack** (MongoDB, Express.js, React.js, Node.js), the system automates attendance and salary calculations across different employee roles, including labour, staff, office boys, guards, and sales personnel.

This guide provides step-by-step instructions for navigating the system’s features, ensuring efficient usage and smooth operation.

---

## Key Features Overview
The Clock Point system offers:

1. **Dashboard**: Overview of attendance metrics.
2. **Employee Management**: Adding, approving, and managing employees.
3. **Attendance Management**: Tracking daily attendance and managing records by employee categories.
4. **Salary Management**: Automated salary calculations, deductions, bonuses, and final salary slips.

---

## Detailed Features

### **1. Dashboard**
The dashboard provides a comprehensive summary of attendance metrics, updated in real-time.

- **Today’s Present**: Number of employees present for the day.
- **Today’s Absent**: Number of employees absent for the day.
- **Available Team**: Employees clocked in (In-Time recorded, but no Out-Time yet).
- **Left**: Employees who have clocked out (In-Time and Out-Time both recorded).

Clicking on any metric provides detailed lists of employees for that category.

---

### **2. Employee Management**
This section enables HR/Admin to manage the entire employee lifecycle, from onboarding to deactivation.

#### **A. Add Employee**
HR/Admin can add new employees by filling out the following fields:

- **Personal Details**: Name, Date of Birth, Mobile Number, Alternate Number, Email, PAN Number, Marital Status, Blood Group, Father’s Name.
- **Address**: Current and Permanent Address, City, Pin Code.
- **Job Details**: Department, Designation, Joining Date, Employee Code, Registration Date, Qualification, Total Experience, Previous Employer.
- **Bank Details**: Account Number, IFSC Code, Branch Name.
- **Salary Details**: Monthly salary.

After submission, the employee is added to the **Pending Employees** section for approval.

#### **B. Pending Employees**
HR/Admin can:
- **Approve Employee**: Moves the employee to the **Trainees** section.
- **Reject Employee**: Permanently deletes the record.
- **Edit Employee**: Update employee details before approval.

#### **C. Trainees**
Approved employees enter a training period before becoming permanent. HR/Admin can:
- **Make Permanent**: Moves the employee to the permanent list.
- **Reject Trainee**: Removes the employee permanently.
- **Edit Trainee**: Update trainee details.

#### **D. All Employees**
Displays all permanent employees. HR/Admin can:
- **Deactivate Employee**: Moves the employee to the **Deactivated Employees** section.
- **Edit Employee**: Modify employee details.

#### **E. Deactivated Employees**
Displays inactive employees. HR/Admin can:
- **Reactivate Employee**: Moves the employee back to the active list.
- **Delete Permanently**: Removes the record from the system.

---

### **3. Attendance Management**
The system allows tracking and recording of daily attendance across all employee categories.

#### **A. Add Attendance**
- Default date is the current day (modifiable).
- Record attendance by selecting **In-Time** and optionally **Out-Time** for each employee.
- Save attendance; records are locked for the day once saved.

#### **B. Attendance by Categories**
The system handles attendance uniquely for each category:

---

#### **Labour Attendance Management**
1. **Salary Calculation**:
   - Based on **hourly rate**.
   - **Daily working hours**: 8 hours.
   - **Default Check-In Time**: 10:00 AM.
   - **Overtime**: Time after 6:30 PM.
   - **Lunch Deduction**: Deduct 30 minutes if arrival is before 2:00 PM; no deduction if arrival is after 2:30 PM.

2. **Rounding Rules**:
   - 1-10 minutes = 0 minutes.
   - 11-25 minutes = 15 minutes.
   - 26-40 minutes = 30 minutes.
   - 41-55 minutes = 45 minutes.

3. **Date-Wise and Month-Wise Attendance**:
   - Track attendance for specific dates or months.
   - Export data to CSV.

---



#### **Office boy Attendance Management**
1. **Salary Calculation**:
   - Based on **hourly rate**.
   - **Daily working hours**: 8 hours.
   - **Default Check-In Time**: 9:00 AM.
   - **Overtime**: Time after 5:30 PM.
   - **Lunch Deduction**: Deduct 30 minutes if arrival is before 2:00 PM; no deduction if arrival is after 2:30 PM.

2. **Rounding Rules**:
   - 1-10 minutes = 0 minutes.
   - 11-25 minutes = 15 minutes.
   - 26-40 minutes = 30 minutes.
   - 41-55 minutes = 45 minutes.

3. **Date-Wise and Month-Wise Attendance**:
   - Track attendance for specific dates or months.
   - Export data to CSV.


#### **Staff Attendance Management**
1. **Salary Calculation**:
   - Based on **daily rate**.
   - **Daily working hours**: 8 hours.
   - **Late Penalty**: Arriving after 10:10 AM for three consecutive days counts as a half-day. Arrivals after 2:30 PM also count as half-days.

2. **Lunch Rules**:
   - Lunch time: 2:00 PM - 2:30 PM.

3. **Rounding Rules**:
   - Same as labour category.

4. **Admin Controls**:
   - Mark holidays or adjust attendance (e.g., half-day to present).

3. **Date-Wise and Month-Wise Attendance**:
   - Track attendance for specific dates or months.
   - Export data to CSV.

---

### **Sales Attendance Management**

1. **Salary Calculation**:
   - Based on **daily rate**.
   - **Daily working hours**: 8 hours.
   - Arrivals after 2:30 PM are considered half-days.

2. **Lunch Rules**:
   - Lunch time is 2:00 PM to 2:30 PM.

3. **Rounding Rules**:
   - Same as labour category.

4. **Admin Controls**:
   - Admin can modify attendance (e.g., change half-day to "Present").

5. **Export Options**:
   - Export total salary to be paid for the month as an Excel file.
   - Export attendance data to CSV.

6. **Sales Date-Wise Attendance**:
   - View attendance for all sales staff on a specific date.
   - Includes options to **edit**, **delete**, and mark half-day as "Present".
   - Export data to CSV.

7. **Sales Month-Wise Attendance**:
   - Displays attendance for a selected sales staff for the selected month.
   - Export data to CSV.


#### **Guard Attendance Management**
1. **Salary Calculation**:
   - Based on **hourly rate**.
   - **Daily working hours**: 12 hours.
   - **Overtime**: Hours worked beyond 12.

2. **Timing Rules**:
   - Standard shifts: 9:00 AM - 9:00 PM or 9:00 PM - 9:00 AM.

3. **Export Options**:
   - Export attendance and salary data to CSV.

3. **Date-Wise and Month-Wise Attendance**:
   - Track attendance for specific dates or months.
   - Export data to CSV.


---

### **4. Salary Management**
The Salary Management Panel handles salary processing, including advances, loans, deductions, and final calculations.

#### **A. Salary Sections**
- **All Salaries**: View details for all employees.
- **Pending Salaries**: Salaries awaiting approval or payment.
- **Remaining Salaries**: Tracks unpaid salaries, considering deductions and bonuses.

#### **B. Advance Payments**
- HR/Admin can provide advance payments to employees.
- Advance amounts are deducted from the base salary.

#### **C. Loan Management**
- Admin can issue loans with monthly installments deducted automatically from salaries.

#### **D. Bonus and Deductions**
- Add bonuses or make deductions for specific employees.

#### **E. Final Salary Calculation**
Formula:
> Final Salary = Base Salary - Loan Deduction - Advance Taken + Bonus - Additional Deduction

Fields displayed include:
- Employee Name and Code.
- Employee Type (e.g., Labour, Staff).
- Base Salary, Loan Deduction, Advance Taken, Bonus, and Total Salary.

#### **F. Salary Slip Generation**
Generate detailed salary slips, including breakdowns of all deductions and bonuses.

---

## Export Options
- **CSV/Excel Exports**: Attendance and salary data can be exported for record-keeping or payroll processing.

---

## Conclusion
The **Clock Point Attendance Management System** is an all-in-one solution for attendance and salary management. By automating attendance tracking, categorizing employees, and providing comprehensive salary calculations, it simplifies HR and payroll operations.

