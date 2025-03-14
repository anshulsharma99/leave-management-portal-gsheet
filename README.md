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

## Manual Deployment Steps

1. **Create a New Google Apps Script Project**
   - Go to [Google Apps Script](https://script.google.com)
   - Click "New Project"
   - Name your project (e.g., "Leave Management System")

2. **Copy Source Files**
   - Create the following files in your Apps Script project:
     * `Code.js`
     * `UI.js`
     * `ManagerInterface.gs`
     * `EmployeeInterface.gs`
     * `SetupInterfaces.gs`
   - Create HTML files:
     * `LeaveRequestForm.html`
     * `MyRequests.html`
     * `PendingRequests.html`
     * `UserManagement.html`
     * `AdminSettings.html`
     * `TeamHistory.html`
     * `AllRequests.html`
   - Copy the contents of each file from this repository to your Apps Script project

3. **Configure Project Settings**
   - Click on "Project Settings" (gear icon)
   - Under "Script Properties", add:
     * `SCRIPT_ID`: Your Apps Script project ID
     * `SPREADSHEET_ID`: ID of your master spreadsheet (will be created in step 5)

4. **Enable Required Google Services**
   - Click on "Services" (+ icon)
   - Add these services:
     * Google Sheets API
     * Gmail API
     * Google Drive API

5. **Create Master Spreadsheet**
   - Create a new Google Spreadsheet
   - Name it "Leave Management System"
   - Copy its ID from the URL (the long string between /d/ and /edit)
   - Add this ID to your script properties as `SPREADSHEET_ID`

6. **Deploy as Web App**
   - Click "Deploy" > "New deployment"
   - Choose "Web app"
   - Set the following:
     * Execute as: "User accessing the web app"
     * Who has access: "Anyone within your organization"
   - Click "Deploy"
   - Authorize the application when prompted

7. **Initialize the System**
   - Open the deployed web app URL
   - Click "Run" > "Run function" > "initializeSystem"
   - Grant necessary permissions when prompted
   - Wait for initialization to complete

## Detailed Usage Guide

### Initial System Setup

1. **First-Time Setup**
   - After deployment, open the web app URL
   - Click "Run" > "Run function" > "initializeSystem"
   - Grant all required permissions when prompted
   - Wait for initialization to complete (you'll see a success message)

2. **Admin Account Setup**
   - The system creates a default admin account using your Google account
   - Access the admin interface through the main spreadsheet
   - You'll see the "Admin Actions" menu in the top bar

[Rest of the usage guide remains the same...]
