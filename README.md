# Leave Management System

A comprehensive leave management solution built entirely in Google Sheets that helps organizations manage employee leave requests, approvals, and tracking. Perfect for small to medium-sized teams who want a simple yet powerful leave management system.

## What This System Does

This system helps you:
- Manage all types of employee leaves (sick leave, vacation, etc.)
- Automate the leave request and approval process
- Track leave balances automatically
- Keep everyone informed through email notifications
- Generate reports and view team calendars
- Maintain a complete audit trail

## Features in Detail

### For Employees
- Submit leave requests easily through a form
- View all your leave requests and their status
- Check your leave balance
- Get email notifications when your request is approved/rejected
- View your leave history

### For Managers
- See all pending leave requests from your team
- Approve or reject requests with comments
- View team calendar to see who's off when
- Track leave patterns and history
- Get email notifications for new requests

### For Admins
- Manage all users and their roles
- Configure leave types and policies
- View system-wide reports and analytics
- Monitor all leave requests across the organization
- Configure system settings

## Step-by-Step Setup Guide

### 1. Create Your Google Sheet
1. Open your web browser and go to [Google Sheets](https://sheets.google.com)
2. Click the plus icon (+) to create a new spreadsheet
3. Click on "Untitled spreadsheet" at the top and name it "Leave Management System"
4. The sheet will auto-save with your new name

### 2. Open the Apps Script Editor
1. In your new spreadsheet, click on "Extensions" in the top menu
2. Click on "Apps Script" from the dropdown menu
3. This opens the Apps Script editor in a new tab
4. The editor will show a default file called "Code.gs"
5. Click on the project name (probably "Untitled project") and rename it to "Leave Management System"

### 3. Create and Copy Code Files
You need to create several files and copy code into them. Here's how:

#### Script Files (.gs):

1. Create these additional script files:
   - Click the plus (+) icon next to "Files"
   - For each file:
     * Click "Script" (not HTML)
     * Name it exactly as shown below
     * Copy code from this repository's corresponding file
     * Click Ctrl+S (or Cmd+S on Mac) to save

Required script files:
- `Code.gs`
- `UI.gs`
- `ManagerInterface.gs`
- `EmployeeInterface.gs`
- `SetupInterfaces.gs`

#### HTML Files:
1. For each HTML file:
   - Click the plus (+) icon next to "Files"
   - Choose "HTML"
   - Name it exactly as shown below
   - Copy code from this repository's corresponding file
   - Click Ctrl+S (or Cmd+S on Mac) to save

Required HTML files:
- `LeaveRequestForm.html`
- `MyRequests.html`
- `PendingRequests.html`
- `UserManagement.html`
- `AdminSettings.html`
- `TeamHistory.html`
- `AllRequests.html`

### Copy the code from the files ins the project onto app script files created

### 4. Initialize the System
1. In the Apps Script editor:
   - Make sure you're on the `Code.js` file
   - Look for the function called `initializeSystemDirect`
   - Click the "Run" button (play icon) at the top
   - If prompted about permissions:
     * Click "Review Permissions"
     * Choose your Google account
     * Click "Allow" for all permissions
2. Wait for initialization to complete
3. You'll see a success message when done

### 5. Verify Setup
1. Go back to your Google Sheet
2. Refresh the page
3. You should see new menus at the top:
   - "Admin Actions" menu
   - "Leave Actions" menu
4. You should also see new sheets created:
   - LeaveRequests
   - UserRoles
   - LeaveTypes
   - AuditLog
   - Settings

## Using the System

### As an Admin

#### Managing Users
1. Click "Admin Actions" > "Manage Users"
2. In the popup window:
   - Click "Add New User" to add someone
   - Fill in their details:
     * Email (must be Google account)
     * Role (Admin/Manager/Employee)
     * Department
     * Manager (for Employees)
     * Allowed leave types
   - Click "Save"
3. The user will receive an email with access details

#### System Settings
1. Click "Admin Actions" > "System Settings"
2. Here you can:
   - Configure leave types
   - Set up departments
   - Adjust email notifications
   - View audit logs

### As a Manager

#### Handling Leave Requests
1. Click "Manager Actions" > "View Pending Requests"
2. For each request:
   - Review the details
   - Add optional comment
   - Click "Approve" or "Reject"
3. The employee will be notified automatically

#### Team Calendar
1. Click "Manager Actions" > "View Team Calendar"
2. See your team's approved leaves
3. Use arrows to navigate months
4. Click on any date for details

### As an Employee

#### Submitting Leave
1. Click "Leave Actions" > "Submit Leave Request"
2. Fill in the form:
   - Select leave type
   - Choose start and end dates
   - Add reason for leave
3. Click "Submit"
4. Your manager will be notified

#### Checking Status
1. Click "Leave Actions" > "View My Requests"
2. See all your requests and their status
3. Click on any request for details

## Troubleshooting

### Common Issues

1. **Menus Not Showing**
   - Refresh the page
   - Make sure initialization completed
   - Check if you're signed in to correct Google account

2. **Can't Submit Request**
   - Check if you have available leave balance
   - Verify dates are correct (not in past)
   - Make sure you have a manager assigned

3. **Email Issues**
   - Check spam folder
   - Verify email address is correct
   - Make sure Gmail API is enabled

4. **Access Problems**
   - Verify you're using correct Google account
   - Ask admin to check your role assignment
   - Try clearing browser cache

For any other issues, check the AuditLog sheet for error messages or contact your system administrator.
