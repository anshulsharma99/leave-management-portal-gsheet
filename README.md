# Leave Management System

A complete leave management solution built with Google Sheets, featuring role-based access control, automated workflows, and email notifications.

## Features

- Role-based access (Admin, Manager, Employee)
- Automated leave request workflow
- Email notifications
- Leave balance tracking
- Team calendar view
- Comprehensive reporting
- Audit logging

## Prerequisites

1. Node.js and npm installed
2. Google account with access to Google Sheets and Apps Script
3. Google Cloud Platform setup:
   - Go to [Google Cloud Console](https://console.cloud.google.com)
   - Create a new project or select existing one
   - Enable these APIs:
     * Google Apps Script API
     * Google Sheets API
     * Gmail API

## Installation

1. Clone this repository:
```bash
git clone <repository-url>
cd googleSheet
```

2. Enable Google Apps Script API:
   - Visit [Google Apps Script Settings](https://script.google.com/home/usersettings)
   - Enable "Google Apps Script API"

3. Make the deployment script executable and run it:
```bash
chmod +x deploy.sh
./deploy.sh
```

## Detailed Usage Guide

### Initial System Setup

1. **First-Time Setup**
   - After deployment, open the script URL provided
   - Click "Run" > "Run function" > "initializeSystem"
   - Grant all required permissions when prompted
   - Wait for initialization to complete (you'll see a success message)

2. **Admin Account Setup**
   - The system creates a default admin account using your Google account
   - Access the admin interface through the main spreadsheet
   - You'll see the "Admin Actions" menu in the top bar

3. **System Configuration**
   - Go to "Admin Actions" > "System Settings"
   - Configure email notifications
   - Set up leave types and policies
   - Define departments and reporting structure

### Admin Guide

1. **Managing Users**
   
   Adding New Users:
   - Click "Admin Actions" > "Manage Users"
   - Click "Add New User" button
   - Fill in required details:
     * Email address
     * Role (Admin/Manager/Employee)
     * Department
     * Manager (for employees)
     * Allowed leave types
   - Click "Save" to create user
   - User will receive access email automatically

   Editing Users:
   - In User Management, find the user
   - Click "Edit" button
   - Update necessary fields
   - Click "Save" to apply changes
   - System will update permissions automatically

   Deleting Users:
   - In User Management, find the user
   - Click "Delete" button
   - Confirm deletion
   - System removes user and revokes access

2. **System Monitoring**
   - View all leave requests: "Admin Actions" > "View All Requests"
   - Check audit logs: "Admin Actions" > "System Settings" > "Audit Log"
   - Monitor system status: "Admin Actions" > "System Settings" > "Status"

3. **Troubleshooting**
   - If menus don't appear: Refresh page or rerun initialization
   - For permission issues: Check user roles in UserRoles sheet
   - Email problems: Verify Gmail API is enabled and check spam folders

### Manager Guide

1. **Accessing Manager Interface**
   - Use the URL received in welcome email
   - Or access through the main spreadsheet if you have admin rights
   - You'll see "Manager Actions" menu

2. **Managing Leave Requests**
   
   Viewing Requests:
   - Click "Manager Actions" > "View Pending Requests"
   - See all pending requests from your team
   - Click on any request for details

   Approving/Rejecting:
   - Open pending request
   - Review details (dates, type, reason)
   - Add optional comment
   - Click "Approve" or "Reject"
   - System sends notification to employee

3. **Team Calendar**
   - Click "Manager Actions" > "View Team Calendar"
   - See all approved leaves in calendar view
   - Use arrows to navigate months
   - Click on dates for details

4. **Reports**
   - Click "Manager Actions" > "View Team History"
   - See complete leave history
   - Filter by date, status, or employee
   - Export data if needed

### Employee Guide

1. **Submitting Leave Requests**
   - Click "Leave Actions" > "Submit Leave Request"
   - Select leave type from available options
   - Choose start and end dates
   - Add reason for leave
   - Click "Submit"
   - System notifies your manager

2. **Checking Request Status**
   - Click "Leave Actions" > "View My Requests"
   - See all your requests and their status
   - Click on any request for details
   - Check manager comments if any

3. **Leave Balance**
   - Click "Leave Actions" > "View Leave Balance"
   - See remaining leaves by type
   - View leave history
   - Check upcoming approved leaves

### Common Operations

1. **Changing User Role**
   - Admin opens User Management
   - Finds user and clicks "Edit"
   - Changes role in dropdown
   - Saves changes
   - System updates permissions and sends notification

2. **Managing Department Structure**
   - Admin opens System Settings
   - Goes to "Departments" tab
   - Adds/edits departments
   - Assigns managers
   - Updates affected users

3. **Leave Type Configuration**
   - Admin opens System Settings
   - Goes to "Leave Types" tab
   - Configures available types
   - Sets limits and policies
   - Assigns to roles/departments

4. **Report Generation**
   - Open respective interface (Admin/Manager)
   - Go to relevant report section
   - Set filters if needed
   - Click "Generate Report"
   - Export or share as needed

### Troubleshooting Guide

1. **Access Issues**
   - Verify email address matches Google account
   - Check role assignment in UserRoles sheet
   - Try clearing browser cache
   - Request admin to resend access

2. **Interface Problems**
   - Refresh page to reload interface
   - Check if system is initialized
   - Verify Google Apps Script is enabled
   - Clear browser cache and cookies

3. **Email Notifications**
   - Check spam folder
   - Verify email address is correct
   - Ensure Gmail API is enabled
   - Check notification settings

4. **Permission Errors**
   - Contact admin to verify role
   - Check if interface URLs are correct
   - Try accessing through main spreadsheet
   - Request admin to reinitialize access

## Development

### Local Development
1. Make changes to files in the `src` directory
2. Push changes using:
```bash
clasp push
```

### Updating Deployed System
1. Push your changes:
```bash
clasp push
```
2. Open the Apps Script editor
3. Verify changes are applied
4. Test functionality in the spreadsheet

## License

[Your License Here]
